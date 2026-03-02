# HW 13.1: API Test Automation (QAuto Project)

This repository contains a Postman collection designed for automated API testing of the **QAuto** web application.

## 🚀 Main Test Flow
The collection implements a complete user lifecycle, ensuring data consistency across multiple requests:
* **Signup**: Registers a unique user every time using a `Pre-request script` to generate dynamic emails and passwords.
* **Edit Profile**: Updates user profile details (Name, Last Name, Country, Birthdate).
* **Change Password**: Implements an automated password update where the `oldPassword` field automatically pulls the value used during registration.
* **Logout / Signin**: Verifies the authentication system by logging out and logging back in with the newly updated credentials.
* **Car Management**: Adds a new vehicle to the user's garage and dynamically captures the `carId` for subsequent tests.
* **Expenses**: Adds fuel/maintenance expenses to the specific car created in the previous step using the stored `carId`.
* **Delete User**: A cleanup step that removes the test user from the system to maintain a clean database.

## ❌ Negative Testing (Field Validation)
A dedicated folder, **"field validation check Password"**, contains tests to verify that the system correctly rejects invalid input with a `400 Bad Request` status:
* **Short Password**: Tests the minimum length requirement.
* **No Digits**: Verifies that passwords must contain at least one number.
* **No Capital Letters**: Checks for uppercase character requirements.
* **Long Password**: Tests the maximum character limit (15 characters).
* **Passwords Don't Match**: Verifies the validation between `password` and `repeatPassword` fields.
* **Empty Password**: Ensures the field cannot be left blank.



## 🛠 Configuration & Environment
* **Environments**: The project includes two environments: `QAuto_Dev.json` and `QAuto_Prod.json`. 
* **Base URL**: Managed via the `{{baseUrl}}` variable, allowing seamless switching between Development and Production servers.
* **Authentication**: `Basic Auth` is configured at the collection level using the required `guest` / `welcome2qauto` credentials.

## 📊 Project Artifacts
The following files and evidence are included in this directory:
* `HM13.1_QA_auto.json`: The full Postman collection.
* `QAuto_Dev.json`: The environment configuration file.
* **Screenshots**: High-resolution images confirming successful execution for each major request (Registration, Login, Car Creation, etc.).

## How to Run
1. Import the **Collection** and **Environment** files into Postman.
2. Select the `QAuto Dev` environment in the top-right corner.
3. Open the **Collection Runner**.
4. Click **Run QAuto Project** to execute all tests automatically.