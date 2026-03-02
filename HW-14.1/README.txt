# HW 14.1: API Testing (User & Garage Management)

This project focuses on advanced API testing scenarios for the **QAuto** application, including complex data validation and multi-step workflows.

## 🚀 Key Testing Scenarios
This collection covers a robust automation flow within the `auto` folder:
* **Registration request**: Validates the creation of a new user account.
* **Data type validation**: Advanced checks to ensure server responses match the expected data schemas (strings, integers, booleans).
* **Logout**: Verifies session termination.
* **Check email value**: Specifically tests the uniqueness and formatting of user email addresses.
* **Car Creates & Car Expense**: Automates the full cycle of adding a vehicle and logging associated fuel/maintenance costs.
* **Field validation query group**: A specialized group of tests for boundary value analysis and field constraints.
* **Editing a user profile**: PUT request to update existing user information.
* **Change password**: Verifies the security workflow for updating user credentials.

## 🛠 Features
* **Automation**: Integrated scripts to handle dynamic data passing between requests.
* **Verification**: Custom test scripts for each endpoint to validate status codes and response bodies.
* **Environment Support**: Designed to work seamlessly with the `QAuto_Dev` environment.

## How to Run
1. Import `HM14.1_QA_auto.json` into Postman.
2. Ensure the `QAuto Dev` environment is active.
3. Open the **Collection Runner** and execute the `auto` folder.