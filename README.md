# FUTURE_CS_03

# API Security Risk Analysis – Task 3 (CS)

## Overview
This project is part of the Future Interns Cyber Security track (Task 3).
The objective is to perform a read-only API security risk analysis on a public
demo API and document identified risks in a professional, business-friendly way.

## API Tested
- Name: JSONPlaceholder
- URL: https://jsonplaceholder.typicode.com
- Endpoint Tested: /users
- Method: GET

## Scope & Ethics
- Public demo API only
- Read-only requests (GET)
- No exploitation or abuse
- No authentication bypass attempts

## Tools Used
- Postman (API request & response inspection)
- Browser (documentation review)
- GitHub (documentation & evidence storage)

## Findings Summary

### 1. Unauthenticated Access to Sensitive Data
- **Description:** The `/users` endpoint returns user information without any authentication.
- **Evidence:** See screenshots in the repository.
- **Risk Level:** Medium
- **Business Impact:** 
  Exposed personal data can be harvested by attackers and misused for phishing,
  identity profiling, or social engineering attacks.

### 2. Excessive Data Exposure
- **Description:** API responses include email addresses, phone numbers, physical addresses, and geo-location data.
- **Risk Level:** Medium
- **Business Impact:**
  Overexposure of user data increases privacy risk and may violate data protection
  best practices if implemented in a real production environment.

## Recommendations
- Require authentication for endpoints returning user data.
- Limit API responses to only necessary fields.
- Implement rate limiting to prevent automated data scraping.
- Apply role-based access control (RBAC) for sensitive resources.

## Conclusion
This assessment demonstrates how unsecured or poorly designed APIs can expose
sensitive information. Proper authentication, authorization, and data minimization
are critical to securing modern SaaS applications.
