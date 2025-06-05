```markdown
# 🧪 RESTful Booker API Testing

A simple project for automated testing of the RESTful Booker API using Postman, Newman, and data-driven testing with CSV files.

## 📁 Project Structure

```

├── restful-booker-api.postman\_collection.json
├── restful-booker-api.postman\_environment.json
├── test-data.csv
└── reports/

````

- **Collection File**: Contains the API test cases.
- **Environment File**: Stores variables for the test environment.
- **CSV File**: Input data for data-driven test runs.
- **Reports Folder**: Stores generated HTML reports.

## 🚀 Getting Started

### Prerequisites

Make sure Node.js and npm are installed on your machine.

Install Newman and the HTML Extra reporter:

```bash
npm install -g newman newman-reporter-htmlextra
````

### Run Tests

```bash
newman run restful-booker-api.postman_collection.json \
  -e restful-booker-api.postman_environment.json \
  -d test-data.csv \
  --iteration-count 20 \
  --delay-request 200 \
  -r cli,html,htmlextra \
  --reporter-html-export reports/basic-report.html \
  --reporter-htmlextra-export reports/detailed-report.html
```

## 📊 Output

* CLI Summary Report
* Basic HTML Report
* Advanced HTML Report (`htmlextra`) with rich visuals and details

## ✅ Purpose

This project demonstrates how to:

* Use Postman for REST API test case creation
* Execute data-driven tests with Newman
* Generate professional HTML reports

---

Feel free to fork this repo or adapt it to test your own API projects!

```
