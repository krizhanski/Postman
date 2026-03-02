# 🚀 Postman API Testing Portfolio | QA PRO Course

Welcome to my Postman repository! This project contains API test collections developed during the **QA PRO** course. It demonstrates practical skills in backend testing, test automation, and API validation using Postman.

## 📂 Repository Structure

The repository is organized by modules/homework assignments. Each folder contains the exported Postman collections, environment configurations, and visual evidence of test executions.

* 📁 **[HW-13.1-QAuto-API](./HW-13.1-QAuto-API)**
  * **Focus:** Basic API flow automation, environment setup, dynamic variables, and negative testing.
  * **Key Scenarios:** Dynamic user registration, authentication (Login/Logout), password validation rules, and basic entity creation (Cars & Expenses).

* 📁 **[HW-14.1-API-Testing](./HW-14.1-API-Testing)**
  * **Focus:** Advanced API testing, strict data type validation, complex assertions, and multi-step workflows.
  * **Key Scenarios:** Boundary value analysis, full user/garage lifecycle management, and dynamic data parsing from server responses.

## 🛠️ Tools & Technologies Used
* **Postman:** Structuring requests, building collections, and managing environments (Dev/Prod).
* **JavaScript (Chai Assertion Library):** Writing `Pre-request Scripts` and Post-response `Tests` for validations.
* **REST API:** Mastering HTTP methods (`GET`, `POST`, `PUT`, `DELETE`), headers, and status code analysis.
* **Git / GitHub:** Version control, branching strategies, and portfolio documentation.

## 💡 Key QA Skills Demonstrated
1. **Dynamic Data Generation:** Writing JS scripts to generate unique emails, passwords, and integer values to prevent test data collisions.
2. **Request Chaining:** Extracting specific data (e.g., `userId` or `carId`) from a response payload and securely passing it to subsequent requests via environment variables.
3. **Negative & Boundary Testing:** Designing targeted error-handling tests (400 Bad Request, 401 Unauthorized) to ensure robust system behavior and proper validation messages.
4. **End-to-End Automation:** Structuring tests so they can be seamlessly executed via the Postman **Collection Runner** with zero manual intervention.

## ⚙️ How to Run Locally
1. Clone this repository to your local machine: 
   ```bash
   git clone [https://github.com/krizhanski/Postman.git](https://github.com/krizhanski/Postman.git)