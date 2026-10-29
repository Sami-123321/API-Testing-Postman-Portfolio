# API Testing — Test Cases

## Project Overview

This document contains test cases for the Idea Center REST API. The test cases cover user authentication, idea management, input validation, negative scenarios, and boundary value testing.

## Test Cases

### Positive Tests

| Test Case ID | Test Scenario                                   | Expected Result                                                |
| ------------ | ----------------------------------------------- | -------------------------------------------------------------- |
| TC-001       | Create a user with valid data                   | The API accepts the request and returns the expected response. |
| TC-002       | Log in with valid credentials                   | Authentication succeeds and an access token is returned.       |
| TC-003       | Retrieve all ideas with valid authentication    | The API returns the list of ideas.                             |
| TC-004       | Create an idea with valid title and description | The idea is created successfully.                              |
| TC-005       | Edit an existing idea                           | The specified idea is updated successfully.                    |
| TC-006       | Delete an existing idea                         | The specified idea is deleted successfully.                    |

### Negative Tests

| Test Case ID | Test Scenario                                                  | Expected Result                                                     |
| ------------ | -------------------------------------------------------------- | ------------------------------------------------------------------- |
| TC-007       | Log in with invalid credentials                                | Authentication fails and an appropriate error response is returned. |
| TC-008       | Create an idea without a title                                 | The API rejects the invalid request.                                |
| TC-009       | Create an idea without a description                           | The API rejects the invalid request.                                |
| TC-010       | Create an idea without an authentication token                 | The API denies the unauthorized request.                            |
| TC-011       | Edit an idea without an authentication token                   | The API denies the unauthorized request.                            |
| TC-012       | Delete an idea without an authentication token                 | The API denies the unauthorized request.                            |
| TC-013       | Submit a title or description below the minimum allowed length | The API validates the input and rejects invalid data.               |
| TC-014       | Submit an invalid URL where a URL is required                  | The API rejects the invalid URL.                                    |

### Edge Cases

| Test Case ID | Test Scenario                                             | Expected Result                                                   |
| ------------ | --------------------------------------------------------- | ----------------------------------------------------------------- |
| TC-015       | Submit a title at the minimum allowed length              | The API accepts the title if it meets the validation rules.       |
| TC-016       | Submit a title at the maximum allowed length              | The API accepts the title if it meets the validation rules.       |
| TC-017       | Submit a title exceeding the maximum allowed length       | The API rejects the title.                                        |
| TC-018       | Submit a description at the minimum allowed length        | The API accepts the description if it meets the validation rules. |
| TC-019       | Submit a description at the maximum allowed length        | The API accepts the description if it meets the validation rules. |
| TC-020       | Submit a description exceeding the maximum allowed length | The API rejects the description.                                  |
| TC-021       | Submit a title with leading or trailing spaces            | The API handles the spaces according to its validation rules.     |

## Test Approach

The test cases use the following testing techniques:

* Positive testing
* Negative testing
* Boundary value analysis
* Input validation
* Authentication testing
* Response validation

## Notes

* Actual response status codes and response bodies should be verified against the API behavior.
* Minimum and maximum input lengths should match the API's documented validation rules.
* Test data and credentials should be kept separate from public project files.
* Never publish passwords, access tokens, or other sensitive information.
