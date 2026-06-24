### Bug Report: Delay When Retrieving External Booking Information

#### Description
The customer profile system freezes when an operator tries to retrieve real-time itinerary and passenger details from an external booking system. The request to the external system fails, causing the application to wait without a response and temporarily stopping the workflow.

#### Environment
* **Platform:** Enterprise Customer Relationship Management (CRM) System
* **Context:** Customer Loyalty Operations -> Historical Booking Retrieval Module

#### Error Message
```text
Error invoking service '[IntegrationService]'.[ERROR_CODE_A] 
Operation '[FetchAction]' is expecting a response but no response was received.[ERROR_CODE_B] 
Error Number: [InternalID] Please contact your system administrator for assistance.[ERROR_CODE_C]
```

#### Steps to Reproduce
1. Log into the CRM platform.
2. Go to the call logging workspace.
3. Enter the required booking details (e.g., ship name, booking reference number, and travel date) in the corresponding fields.
4. Click Retrieve Booking.
5. Observe the system freezing briefly before showing a connection error message.

#### Expected Behavior
The system should successfully request booking information from the external system and display the related passenger and itinerary details so the user can continue processing loyalty actions.

#### Actual Behavior
The external system does not respond, causing the request to fail with [ERROR_CODE_B]. As a result, the screen becomes unresponsive and the user is unable to retrieve passenger details or continue the workflow.

