# API Testing — Bug Reports

## Overview

This document demonstrates how API defects can be documented during software testing. The examples below are illustrative templates and must be verified against the actual API before being reported as confirmed defects.

## Bug Report Template

* **Bug ID:**
* **Title:**
* **Environment:**
* **Preconditions:**
* **Steps to Reproduce:**
* **Expected Result:**
* **Actual Result:**
* **Severity:**
* **Priority:**
* **Status:**

---

## Example 1 — Missing Title Validation

**Bug ID:** BR-001

**Title:** API accepts an idea without a title

**Environment:** Idea Center API, tested using Postman

**Preconditions:** A valid user account and authentication token are available.

**Steps to Reproduce:**

1. Send a POST request to `/api/Idea/Create`.
2. Include a valid authentication token.
3. Submit a request body with the title missing.
4. Inspect the response.

**Expected Result:** The API rejects the request and returns an appropriate validation error.

**Actual Result:** To be recorded after executing the test.

**Severity:** To be determined after verification.

**Priority:** To be determined after verification.

**Status:** Not verified

---

## Example 2 — Missing Authentication

**Bug ID:** BR-002

**Title:** Idea creation endpoint may allow an unauthenticated request

**Environment:** Idea Center API, tested using Postman

**Preconditions:** No authentication token is provided.

**Steps to Reproduce:**

1. Send a POST request to `/api/Idea/Create`.
2. Do not include an authentication token.
3. Submit an otherwise valid request body.
4. Inspect the response and verify whether an idea was created.

**Expected Result:** The API rejects the unauthorized request.

**Actual Result:** To be recorded after executing the test.

**Severity:** To be determined after verification.

**Priority:** To be determined after verification.

**Status:** Not verified

---

## Reporting Guidelines

* Use clear, concise bug titles.
* Include reproducible steps.
* Record the actual response status code and response body.
* Compare the actual result with the expected result.
* Assign severity and priority based on verified impact.
* Never report an unverified example as a confirmed defect.
* Do not include passwords, access tokens, or other sensitive data in reports.
