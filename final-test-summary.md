# Toolshop — Final Test Summary

## 1. Test Overview

- **Application:** Toolshop — With Bugs
- **Test Type:** Manual Functional Testing + API Testing
- **Environment:** Web browser / Desktop
- **Scope:** Authentication, product catalog, product search/filtering, product details, shopping cart, API behavior, and selected DevTools investigations.

## 2. Execution Summary

A total of **23 manual test cases** were defined.

| Result | Count |
|---|---:|
| PASS | 6 |
| FAIL | 4 |
| NOT EXECUTED | 13 |
| **Total** | **23** |

Targeted exploratory testing was also performed to investigate observed application behavior.

API testing was performed using Postman with **10 API tests**, covering product retrieval, filtering, sorting, product search, catalog resources, and authentication.

## 3. Defects Identified

### BUG-001 — Cart Controls Do Not Modify Cart Contents

The `+`, `−`, and remove controls did not perform their expected actions.

- **Severity:** Medium
- **Priority:** High
- **Related Test Cases:** TC-17, TC-18, TC-20

### BUG-002 — Add-to-Cart Displays Error Despite Successful Addition

A product was successfully added to the cart while the application simultaneously displayed a **"Something went wrong"** message.

- **Severity:** Medium
- **Priority:** High
- **Related Test Case:** TC-15

## 4. Key Findings

- Core product browsing functionality was operational.
- Product search and category filtering were observed working.
- Product details displayed correctly during testing.
- Cart management contained significant functional issues.
- The add-to-cart operation produced contradictory user feedback.
- Manual quantity entry remained functional despite the `+` and `−` controls failing.
- API endpoints tested through Postman generally returned the expected HTTP behavior.
- DevTools investigations did not establish a confirmed root cause for the cart-related issues.

## 5. Test Limitations

- Authentication flows were not fully executed because a complete registration/login workflow was outside the targeted manual execution scope.
- Checkout completion was not executed because valid payment/order data was not required for the project scope.
- Database-level validation was not performed because direct database access was unavailable.
- Only selected DevTools investigations were performed.

Therefore, the results should **not** be interpreted as complete system certification.

## 6. Overall Assessment

Testing identified functional issues affecting important shopping-cart operations.

The application demonstrated generally functional product browsing, search/filtering, and the tested API functionality. However, the identified cart defects should be addressed and retested before the affected functionality is considered ready for release.

**Overall QA Assessment:**  
**Conditional — further investigation and retesting are recommended before release of the affected cart functionality.** 
