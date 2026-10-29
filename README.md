# API Testing Portfolio — Postman

## About the Project

This project demonstrates my practical skills in REST API testing using Postman. It focuses on validating API functionality, response status codes, response bodies, authentication, input validation, and error handling.

The project uses the **Idea Center API** as the system under test.

## Tools and Technologies

* **Postman** — API requests and test scripts
* **JavaScript** — writing Postman test assertions
* **Git and GitHub** — version control and project documentation
* **REST API** — HTTP methods and request/response validation

## Test Coverage

### 1. Positive Tests

* Create a user
* Log in and retrieve an authentication token
* Create a new idea
* Retrieve all ideas
* Edit an existing idea
* Delete an idea

### 2. Negative Tests

* Login with invalid credentials
* Validate missing or invalid input
* Test title and description length restrictions
* Test requests without authentication
* Validate API error responses

### 3. Edge Cases

* Minimum and maximum title lengths
* Minimum and maximum description lengths
* Titles containing leading or trailing spaces
* Overlong title and description values

## API Endpoints Covered

| Method | Endpoint                   | Purpose             |
| ------ | -------------------------- | ------------------- |
| POST   | `/api/User/Create`         | Create a user       |
| POST   | `/api/User/Authentication` | Authenticate a user |
| GET    | `/api/Idea/All`            | Retrieve ideas      |
| POST   | `/api/Idea/Create`         | Create an idea      |
| PUT    | `/api/Idea/Edit`           | Edit an idea        |
| DELETE | `/api/Idea/Delete`         | Delete an idea      |

## Testing Techniques

* HTTP status code validation
* Response body assertions
* Authentication and token handling
* Positive and negative testing
* Boundary value testing
* Input validation
* Collection and environment variables
* Pre-request scripts and test scripts

## How to Run the Tests

1. Download or clone this repository.
2. Open Postman.
3. Import `Idea Center API Tests.postman_collection.json`.
4. Configure the required environment variables for authentication.
5. Select the collection or a specific folder.
6. Run the requests and review the test results.

**Note:** Configure valid credentials and variables before running the tests. Never commit passwords, access tokens, or other sensitive information to GitHub.

## Project Structure

```text
API-Testing-Postman-Portfolio/
├── README.md
└── Idea Center API Tests.postman_collection.json
```

## Author

Aspiring Junior QA Engineer interested in software testing, API testing, and test automation.
