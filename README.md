# 🚀 API Testing Portfolio | QA PRO Course

Welcome to my comprehensive QA portfolio repository! This project contains API test collections and infrastructure setups developed during the **QA PRO** course. It demonstrates practical skills in backend testing, test automation, performance evaluation, CI/CD integration, and database modeling.

## 📂 Repository Structure

The repository is organized by modules and homework assignments. Each folder contains exported collections, environment configurations, and documentation.

### 📁 [HW-13.1-QAuto-API](./HW-13.1)
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

### 📁 [HW-22.1-Performance-Optimization](./HW-22.1)
**Focus:** Dynamic data correlation, infrastructure resource monitoring (PerfMon), and environment troubleshooting.
**Key Scenarios:** Extracting dynamic values (system-generated IDs) from `POST` responses using JSON Extractors to feed subsequent `DELETE` requests, monitoring OS-level CPU/Memory via ServerAgent, resolving service port collisions (Jenkins CI vs. Target API on port `8080`), and verifying system stability and throughput under concurrent loads.

### 📁 [HW-23.1-MongoDB-Migration](./HW-23.1)
**Focus:** NoSQL Database Design, SQL to MongoDB data migration, relational mapping via Referencing, and data integrity enforcement.
**Key Scenarios:** Deploying a local MongoDB server via Homebrew, modeling 1:1 (Users/UserProfile) and One-to-Many (Brands/Models) relationships using `ObjectId` referencing, executing CRUD operations via `mongosh`, troubleshooting and resolving data duplication issues through surgical cleanup, and exporting collections to JSON.

---

## 🛠️ Tools & Technologies Used

* **Performance Testing & Monitoring:** Apache JMeter (CLI mode), PerfMon Server Agent.
* **Databases:** MongoDB Community Server, MongoDB Compass.
* **Containerization:** Docker.
* **CI/CD:** Jenkins (LTS), Homebrew, Shell Scripting.
* **Postman:** Request structuring, Collection Runner, and Environment management.
* **Testing Protocols:** REST, GraphQL, SOAP (XML).
* **Automation:** JavaScript (Chai Assertion Library).
* **Version Control:** Git & GitHub.

## 💡 Key QA Skills Demonstrated

* **Load & Stress Testing:** Designing JMeter test plans, executing extreme concurrency tests via CLI, and interpreting performance metrics (Throughput, Response Time, Error Rates).
* **Dynamic Data Correlation:** Implementing JSON Extractors to capture and seamlessly pass dynamic variables (like object IDs) between concurrent requests to simulate complete user journeys without polluting the database.
* **Database Modeling & Administration:** Transitioning relational SQL logic to document-oriented MongoDB structures using Object-Id referencing, performing CRUD operations via CLI (`mongosh`), and maintaining data integrity by troubleshooting duplicates.
* **Infrastructure Monitoring & Troubleshooting:** Tracking host-level CPU and Memory utilization during load tests using PerfMon, and debugging service port collisions (e.g., re-routing a Dockerized test environment to bypass a Jenkins CSRF block).
* **Environment Virtualization:** Deploying and managing local REST APIs using Docker containers to create isolated testing environments.
* **CI/CD Foundation:** Setting up automation servers, managing plugins, and automating test reports.
* **Data Generation:** Writing JS and JMeter scripts to generate unique test data to prevent database collisions.
* **Negative & Boundary Testing:** Designing robust error-handling tests (400, 401, 403) to ensure system stability.
* **API Contract Testing:** Writing strict assertions to verify that server responses match expected JSON/XML Schemas.

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
5.  **For JMeter Correlation & PerfMon (HW-22.1):**
    * Start the target API on port 3001 (avoiding Jenkins on 8080): `docker run -d -p 3001:3001 oleksandrgolubishko/qa_pro_rest_app`
    * Start PerfMon ServerAgent on port 4444: `./startAgent.sh`
    * Run tests via CLI: `jmeter -n -t Heroes_v22.jmx -l results_v22.jtl -e -o ./report_v22_final`
6.  **For MongoDB Migration (HW-23.1):**
    * Install and start MongoDB via Homebrew: `brew install mongodb-community && brew services start mongodb-community`
    * Connect to `mongodb://localhost:27017` using MongoDB Compass.
    * Create a database named `qauto` and import the provided `.json` collection files.
---
*Completed as part of the practical assignments in the QA PRO Course, 2025-2026.*