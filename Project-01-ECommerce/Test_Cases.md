# Test Matrix: OWASP Juice Shop

## 1. Document Control

| Version | Date | Author | Description |
| :---: | :---: | :---: | :---: |
| v1.0 | June 23, 2026 | Brandon Cabrera | Initial test suite for core web functionalities |

## 2. Test Cases

| Test Case ID | Module | Test Case Description | Preconditions | Execution Steps | Expected Result | Status (Pass/Fail) |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **TC-001** | Authentication | Validate error alerts when registering with empty mandatory fields. | User is not logged in. | 1. Navigate to the top-right menu, click **Account**, then **Login**.<br>2. Click the **"Not yet a customer?"** link at the bottom.<br>3. Leave all mandatory fields empty.<br>4. Attempt to click the register button. | The system must display validation error messages in red. The register button must remain disabled. | Pass |
| **TC-002** | Search Engine | Verify system stability and error handling when searching with special characters. | User is on the home page. | 1. Click the magnifying glass icon to open the search bar.<br>2. Type special characters (e.g., `<>` or `""`).<br>3. Press Enter or trigger the search. | The application must handle the input gracefully. It must not crash, throw a 500 Internal Server Error, or expose raw code. It should display a "No results found" message. | |
| **TC-003** | Shopping Cart | Validate that the shopping cart prevents negative item quantities. | At least one item must be added to the shopping cart. | 1. Navigate to the shopping cart page.<br>2. Manually change the quantity of any item to a negative value (e.g., `-2`).<br>3. Observe the item quantity and the cart's total price. | The system must block negative inputs, reset the quantity to 1, or throw an error. The total price must never become negative or zero. | |
