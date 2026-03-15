# 🚀 Postman API Testing Portfolio | QA PRO Course

Welcome to my Postman repository! This project contains API test collections developed during the **QA PRO** course. It demonstrates practical skills in backend testing, test automation, and API validation using Postman.

## 📂 Repository Structure

The repository is organized by modules/homework assignments. Each folder contains the exported Postman collections, environment configurations, and visual evidence of test executions.

### 📁 [HW-13.1-QAuto-API](./HW-13.1-QAuto-API)
**Focus:** Basic API flow automation, environment setup, dynamic variables, and negative testing.  
**Key Scenarios:** Dynamic user registration, authentication (Login/Logout), password validation rules, and basic entity creation (Cars & Expenses).

### 📁 [HW-14.1-API-Testing](./HW-14.1)
**Focus:** Advanced API testing, strict data type validation, complex assertions, and multi-step workflows.  
**Key Scenarios:** Boundary value analysis, full user/garage lifecycle management, and dynamic data parsing from server responses.

### 📁 [HW-15.1-Collection-Automation](./HW-15.1)
**Focus:** Advanced collection orchestration, dynamic request looping (DRY principle), and multi-iteration environment switching.  
**Key Scenarios:** Automated field validation using `postman.setNextRequest`, dynamic data injection via JSON arrays, and seamless execution across multiple test environments (**qauto** & **qauto2**).

### 📁 [HW-16.1-GraphQL-API-Testing](./HW-16.1)
**Focus:** GraphQL API interaction, query optimization (aliases and fragments), advanced Postman scripting (array manipulation, math functions), and JSON Schema validation.  
**Key Scenarios:** Extracting dynamic values (min/max/average) from queries, passing array variables between requests, batching queries with aliases to prevent overfetching, and automating end-to-end data flow in Collection Runner.

### 📁 [HW-18.1-SOAP-API-Testing](./HW-18.1)
**Focus:** SOAP API interaction, XML payload structuring, XML-to-JSON conversion (`xml2Json`), and deep response parsing.  
**Key Scenarios:** Constructing valid `soap:Envelope` and `soap:Body` requests, validating complex ISBN-10 and ISBN-13 checksum logic, extracting deeply nested XML nodes using JavaScript, asserting XML namespace correctness, and verifying HTTP headers alongside the response body.

---

## 🛠️ Tools & Technologies Used

* **Postman:** Structuring requests, building collections, and managing environments (Dev/Prod).
* **JavaScript (Chai Assertion Library):** Writing *Pre-request Scripts* and Post-response *Tests* for validations.
* **REST API:** Mastering HTTP methods (GET, POST, PUT, DELETE), headers, and status code analysis.
* GraphQL API: Querying and mutating data, utilizing advanced features like Aliases and Fragments to optimize network requests and prevent overfetching.
* **Git / GitHub:** Version control, branching strategies, and portfolio documentation.
* **SOAP API:** Structuring XML payloads (Envelopes and Bodies), interacting with web service endpoints, and asserting XML responses.
* **XML / JSON Parsing:** Utilizing Postman's built-in `xml2Json()` method to convert complex XML responses into easily navigable JavaScript objects for testing.

## 💡 Key QA Skills Demonstrated

* **Dynamic Data Generation:** Writing JS scripts to generate unique emails, passwords, and integer values to prevent test data collisions.
* **Request Chaining:** Extracting specific data (e.g., `userId` or `carId`) from a response payload and securely passing it to subsequent requests via environment variables.
* **Negative & Boundary Testing:** Designing targeted error-handling tests (400 Bad Request, 401 Unauthorized) to ensure robust system behavior and proper validation messages.
* **End-to-End Automation:** Structuring tests so they can be seamlessly executed via the Postman *Collection Runner* with zero manual intervention.
* **Advanced Array Manipulation: Using JavaScript to parse complex JSON responses, extract specific arrays, and perform mathematical operations (like calculating minimum, maximum, and average values) to drive subsequent test logic.
* **GraphQL Query Optimization: Validating batch data retrieval in a single request using Aliases, ensuring the API handles complex, multi-layered queries correctly.
* **API Contract Testing: Writing strict assertions to verify that the server response exactly matches the expected JSON Schema (e.g., verifying id is a string and square is a number), preventing silent data corruption.
* **SOAP & XML Validation:** Crafting valid SOAP requests, parsing nested XML responses, and writing strict assertions for specific nodes and namespaces (e.g., verifying `xmlns` attributes).
* **Comprehensive Test Coverage:** Designing 10+ granular tests per endpoint, ensuring both HTTP-level attributes (headers, status code, response time) and deep payload data (body content, boolean results) are thoroughly verified.


## ⚙️ How to Run Locally

Clone this repository to your local machine:
```bash
git clone [https://github.com/krizhanski/Postman.git](https://github.com/krizhanski/Postman.git)
