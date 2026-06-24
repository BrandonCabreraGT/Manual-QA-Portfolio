# Test Plan: OWASP Juice Shop Security & Functionality QA Project

## 1. Introduction & Objectives
This test plan defines the strategy, scope, and approach for evaluating the core web functionalities and basic security controls of the OWASP Juice Shop application. The primary goal is to identify functional defects and potential security vulnerabilities in critical user workflows.

## 2. Scope of Testing

### In Scope (What is tested)
* **Authentication Module:** User registration validation and login field constraints.
* **Search Engine:** Input validation, sanitization of special characters, and search result accuracy.
* **Shopping Cart & Checkout:** Quantity controls, price calculations, and boundary value management.

### Out of Scope (What is NOT tested)
* Third-party payment gateway integrations.
* Performance, stress, and load testing under high traffic concurrency.
* Mobile responsive layout validation (Testing is strictly desktop-focused for this phase).

## 3. Test Strategy & Types of Testing
* **Functional Testing:** Black-box testing to verify that user paths (Registration, Search, Cart) behave according to expected business logic.
* **Boundary Value Analysis (BVA):** Applied to the shopping cart quantities (e.g., testing negative numbers, zero, and maximum limits).
* **Security/Sanitization Testing:** Input validation tests on the search bar to detect missing encoding or escaping rules.

## 4. Environment & Tools
* **Test Environment:** QA / Production Web App (https://juice-shop.herokuapp.com)
* **Browsers:** Google Chrome Version 149.0.7827.116
* **Documentation Tools:** GitHub Markdown for Test Cases Matrix and Defect Tracking.

## 5. Entry & Exit Criteria

### Entry Criteria
* The target web application URL is stable and publicly accessible.
* Core functionalities (Sign-up, Search, Cart) are deployed and operational.

### Exit Criteria
* 100% of the documented test cases in `Test_Cases.md` have been executed.
* All identified Critical and High priority defects are reported with clear visual evidence.
* A summary of open defects is linked and categorized by severity.

## 6. Deliverables
* `Test_Plan.md` (This document)
* `Test_Cases.md` (Detailed test suite execution matrix)
* `BUG-001.md` (Individual defect logs with steps to reproduce; additional reports will follow the `BUG-XXX.md` naming convention)

