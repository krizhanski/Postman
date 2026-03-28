# 🚀 API Testing Portfolio | QA PRO Course

Welcome to my comprehensive QA portfolio repository! This project contains API test collections and infrastructure setups developed during the **QA PRO** course. It demonstrates practical skills in backend testing, test automation, performance evaluation, and CI/CD integration.

## 📂 Repository Structure

The repository is organized by modules and homework assignments. Each folder contains exported collections, environment configurations, and documentation.

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

### 📁 [HW-20.1-Jenkins-CI-CD](./HW-20.1)
**Focus:** Continuous Integration, environment automation, and build stability.
**Key Scenarios:** Deploying Jenkins LTS on macOS, automating environment readiness checks, configuring build triggers, and implementing **HTML/JUnit test reporting** for automated feedback loops.

### 📁 [HW-21.1-JMeter-Load-Testing](./HW-21.1)
**Focus:** API Load & Stress Testing, Performance bottleneck analysis, CLI execution (Non-GUI), and Containerized test environments.
**Key Scenarios:** Deploying a local Node.js API using Docker, scripting JMeter Test Plans (`.jmx`) with dynamic payload generation to avoid DB collisions, executing progressive load tests (100 to 10,000 threads), implementing `Duration Assertions` for stress testing, generating interactive HTML dashboards, and analyzing OS-level resource limitations (thread exhaustion).

---

## 🛠️ Tools & Technologies Used

* **Performance Testing:** Apache JMeter (CLI mode).
* **Containerization:** Docker.
* **CI/CD:** Jenkins (LTS), Homebrew, Shell Scripting.
* **Postman:** Request structuring, Collection Runner, and Environment management.
* **Testing Protocols:** REST, GraphQL, SOAP (XML).
* **Automation:** JavaScript (Chai Assertion Library).
* **Version Control:** Git & GitHub.

## 💡 Key QA Skills Demonstrated

* **Load & Stress Testing:** Designing JMeter test plans, executing extreme concurrency tests via CLI, and interpreting performance metrics (Throughput, Response Time, Error Rates).
* **Environment Virtualization:** Deploying and managing local REST APIs using Docker containers to create isolated testing environments.
* **CI/CD Foundation:** Setting up automation servers, managing plugins, and automating test reports.
* **Dynamic Data Generation:** Writing JS and JMeter scripts to generate unique test data (emails, passwords, names) to prevent database collisions.
* **Request Chaining:** Seamlessly passing data (IDs, Tokens) between requests via environment variables.
* **Negative & Boundary Testing:** Designing robust error-handling tests (400, 401, 403) to ensure system stability.
* **API Contract Testing:** Writing strict assertions to verify that server responses match expected JSON/XML Schemas.
* **Complex Parsing:** Mastering `xml2Json` and advanced array manipulation to drive test logic.

---

## ⚙️ How to Run Locally

1.  **Clone this repository:**
    ```bash
    git clone [https://github.com/krizhanski/API-Testing_QA-PRO-Course.git](https://github.com/krizhanski/API-Testing_QA-PRO-Course.git)
    ```
2.  **For Postman Collections:** Import the `.json` files from the respective folders into your Postman Desktop app.
3.  **For Jenkins Setup:** * Ensure you have Java 17+ installed.
    * Run `brew services start jenkins-lts` (on macOS).
    * Access the dashboard at `http://localhost:8080`.
4.  **For JMeter Load Tests (HW-21.1):**
    * Start the target API: `docker run -d -p 3001:3001 oleksandrgolubishko/qa_pro_rest_app`
    * Navigate to the folder and run tests via CLI: `jmeter -n -t Heroes.jmx -l results.jtl -e -o ./report`

---
*Completed as part of the practical assignments in the QA PRO Course, 2025-2026.*