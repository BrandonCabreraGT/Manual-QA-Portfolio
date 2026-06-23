# Test Cases Matrix - E-Commerce Platform

**Project:** E-Commerce Web Application  
**Version:** v1.0.0  
**Environment:** QA / Staging  
**Author:** Brandon Cabrera  

---

## Module: User Authentication

### TC-001: Successful Login with Valid Credentials
*   **Description:** Verify that a registered user can successfully log in using a valid email and password.
*   **Pre-conditions:** The user must have a previously registered and active account.
*   **Test Steps:**
    1. Navigate to the login page.
    2. Enter a valid registered email in the "Email" field.
    3. Enter the correct password in the "Password" field.
    4. Click the "Login" button.
*   **Expected Result:** The user is successfully authenticated and redirected to the main dashboard. A welcome message is displayed.
*   **Status:** [Pending / Passed / Failed]

### TC-002: Login Failure with Incorrect Password
*   **Description:** Verify that the system prevents login and displays an appropriate error message when an incorrect password is entered.
*   **Pre-conditions:** The email entered must belong to an active registered account.
*   **Test Steps:**
    1. Navigate to the login page.
    2. Enter a valid registered email.
    3. Enter an incorrect password.
    4. Click the "Login" button.
*   **Expected Result:** The system blocks authentication, keeps the user on the login page, and displays the error message: *"Invalid email or password"*.
*   **Status:** [Pending / Passed / Failed]

---

## Module: Shopping Cart & Checkout

### TC-003: Add Product to Shopping Cart
*   **Description:** Verify that a user can successfully add an available item to the shopping cart from the product detail page.
*   **Pre-conditions:** The user is on a product detail page of an item with active stock.
*   **Test Steps:**
    1. Select the desired quantity (e.g., 1).
    2. Click the "Add to Cart" button.
    3. Click on the shopping cart icon in the top header.
*   **Expected Result:** A confirmation toast message appears (*"Item added successfully"*). The cart icon badge increments by 1, and the specific item is listed in the cart summary with the correct price.
*   **Status:** [Pending / Passed / Failed]

### TC-004: Checkout Process with Empty Required Fields
*   **Description:** Verify that the checkout form validation prevents order submission if mandatory fields (like shipping address) are blank.
*   **Pre-conditions:** The user has at least one item in the shopping cart and is on the Checkout page.
*   **Test Steps:**
    1. Leave the "Shipping Address" and "Phone Number" fields empty.
    2. Select a valid payment method.
    3. Click the "Place Order" button.
*   **Expected Result:** The order is not processed. The missing fields are highlighted in red with validation messages stating: *"This field is required"*.
*   **Status:** [Pending / Passed / Failed]

