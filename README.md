# Toolshop QA Project

A compact end-to-end QA portfolio project demonstrating manual functional testing, exploratory testing, API testing, defect reporting, and browser DevTools investigation on the Toolshop web application.

## Project Overview

The project focuses on validating core e-commerce functionality and identifying defects through realistic QA workflows.

Testing covered:

- Product catalog
- Product search
- Product filtering
- Product details
- Shopping cart
- Quantity management
- Product removal
- Authentication-related flows
- Selected checkout behavior
- REST API functionality
- Browser DevTools investigation

## Testing Approach

The project combines:

- Manual functional testing
- Exploratory testing
- Positive and negative test scenarios
- API testing with Postman
- Browser DevTools inspection
- Structured defect reporting

The testing process focused on observable application behavior. When functionality could not be fully executed because required credentials, payment information, or backend access were unavailable, the relevant cases were explicitly marked as **NOT EXECUTED**.

## Test Results

### Manual Testing

| Result | Count |
|---|---:|
| PASS | 6 |
| FAIL | 4 |
| NOT EXECUTED | 13 |
| **Total** | **23** |

### API Testing

**10 API tests** were executed using Postman.

The collection covers:

- Product retrieval
- Product filtering
- Product sorting
- Product search
- Product details
- Related products
- Authentication
- Negative authentication behavior

All 10 API tests passed.

## Defects Identified

### BUG-001 — Cart Controls Do Not Modify Cart Contents

The cart `+`, `−`, and remove controls did not perform their expected actions.

**Severity:** Medium  
**Priority:** High

### BUG-002 — Add-to-Cart Displays Error Despite Successful Addition

A product was successfully added to the cart while the application simultaneously displayed a **"Something went wrong"** message.

**Severity:** Medium  
**Priority:** High

## DevTools Investigations

Two targeted DevTools investigations were performed:

1. **Add-to-Cart Error Behavior**
   - Network monitoring was used to investigate the unexpected error message.
   - No new visible network request was observed during the action.
   - The product was nevertheless added successfully.

2. **Cart Quantity Controls**
   - The quantity increase control was inspected in the DOM.
   - Relevant `id` and `data-test` attributes were documented.
   - The control was present, but the expected quantity update did not occur when clicked.

## Project Structure

```text
toolshop-qa-project/
├── api/
│   └── Toolshop QA - API Tests.postman_collection.json
├── bug-reports/
│   ├── BUG-001-cart-quantity-controls.md
│   └── BUG-002-add-to-cart-error-message.md
├── devtools/
│   └── investigations.md
├── final-test-summary.md
├── test-cases.md
├── test-plan.md
├── test-scenarios.md
├── test-execution.md
└── README.md
```

## Tools

- **Postman** — REST API testing and assertions
- **Browser DevTools** — DOM and Network investigation
- **Markdown** — QA documentation
- **Git / GitHub** — Project version control and portfolio presentation

## Test Artifacts

- [Test Plan](test-plan.md)
- [Test Scenarios](test-scenarios.md)
- [Test Cases](test-cases.md)
- [Test Execution Results](test-execution.md)
- [Final Test Summary](final-test-summary.md)
- [DevTools Investigations](devtools/investigations.md)
- [Bug Reports](bug-reports/)
- [Postman API Collection](api/Toolshop%20QA%20-%20API%20Tests.postman_collection.json)

## Limitations

- Authentication flows were not fully executed.
- Checkout completion and payment processing were not validated.
- Database-level validation was not performed because direct database access was unavailable.
- Cross-browser, performance, accessibility, and security testing were outside the project scope.
- The results represent targeted QA testing rather than complete system certification.

## Overall QA Assessment

The application demonstrated generally functional product browsing, search/filtering, and tested API behavior.

However, significant issues were identified in shopping-cart functionality, including non-functional cart controls and contradictory add-to-cart feedback. 

The affected cart functionality should be addressed and retested before release.