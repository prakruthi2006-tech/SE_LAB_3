# Lab 3 – Component Modelling & Architectural Pattern Selection

## Objective

The objective of this lab is to evaluate different architectural styles, select a suitable architecture for the assigned scenario, and create a UML Component Diagram showing the components, interfaces, and dependencies.

## Scenario

### Self-Service Coffee Kiosk System

The system is designed for a self-service coffee kiosk in a busy café.

The kiosk allows customers to:

- Select coffee types:
  - Espresso
  - Americano
  - Latte
- Select drink size:
  - Small
  - Large
- Pay using a credit card.
- Receive a printed receipt containing order details.

### Technical Requirements

- Support touchscreen interface interactions.
- Connect to a receipt printer.
- Store menu data and pricing information.

## Architectural Style Selected

### Layered Architecture

Layered Architecture was selected for the Self-Service Coffee Kiosk System.

The system is organized into logical components with separate responsibilities for user interaction, order processing, payment processing, data storage, and receipt printing.

### Reasons for Selection

1. **Separation of Concerns**

   Each component performs a specific responsibility. The Kiosk UI handles touchscreen interaction, while the Order Manager handles order processing and the Payment Service handles payment processing.

2. **Easy Maintenance**

   The modular structure makes the system easier to maintain and modify. Individual components can be changed without requiring changes to the complete system.

## Security Advantage

The Payment Service is separated from the user interface and handles payment-processing operations. This helps restrict access to payment-related functionality and allows payment information to be handled securely.

## Performance Benefit

Separating the user interface from order processing, payment processing, and database operations helps organize system operations and allows the touchscreen interface to remain responsive.

## Component Diagram

The UML Component Diagram contains the following five components:

1. **Kiosk UI**
2. **Order Manager**
3. **Payment Service**
4. **Menu & Pricing Database**
5. **Receipt Printer**

## Component Responsibilities

| Component | Responsibility |
|---|---|
| Kiosk UI | Handles touchscreen interaction and customer order selection |
| Order Manager | Processes and manages customer orders |
| Payment Service | Processes credit card payments |
| Menu & Pricing Database | Stores menu items and pricing information |
| Receipt Printer | Prints the completed order receipt |

## Interfaces

The component diagram contains the following interfaces:

| Interface | Description |
|---|---|
| Order Processing API | Communication between Kiosk UI and Order Manager |
| Payment Processing API | Sends payment processing requests from Order Manager to Payment Service |
| Payment Status | Returns payment status from Payment Service to Order Manager |
| Menu Database Query | Retrieves menu and pricing information |
| Printer Hardware Interface | Sends order details from Order Manager to Receipt Printer |

## UML Notation

The component diagram uses UML component notation and represents:

- Components
- Provided interfaces
- Required interfaces
- Component connections
- Interface labels
- Dependencies and data flow

## Files Included

- `Lab3_Component_Diagram.drawio` – Editable Draw.io source file
- `Lab3_Component_Diagram.png` – Component diagram in PNG format
- `Lab3_Component_Diagram.pdf` – Component diagram in PDF format
- `Lab3_Architecture_Justification.docx` – Architecture justification document
- `Lab3_Architecture_Justification.pdf` – Architecture justification in PDF format

## Conclusion

The lab demonstrates component modelling and architectural pattern selection for a Self-Service Coffee Kiosk System. The selected Layered Architecture separates the major responsibilities of the system into independent components and shows their interactions through UML interfaces and dependencies.
