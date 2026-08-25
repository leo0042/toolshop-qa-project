# Toolshop — Test Plan

## 1. Objective

Validate the core functionality of the Toolshop web application from a QA perspective, with emphasis on product discovery, shopping-cart behavior, authentication-related flows, and selected API functionality.

The goal is to identify functional defects, document test evidence, and provide a concise assessment of the application's current quality.

## 2. Scope

### In Scope

- Product catalog
- Product search
- Product filtering
- Product details
- Shopping cart
- Product quantity management
- Product removal from cart
- User registration and login interface
- Selected checkout behavior
- REST API validation using Postman
- Browser DevTools investigation
- Functional and negative testing

### Out of Scope

- Payment processing validation
- Complete order placement
- Database-level validation
- Performance testing
- Security penetration testing
- Cross-browser compatibility testing
- Accessibility compliance testing

## 3. Test Approach

Testing was performed using a combination of:

- Manual functional testing
- Exploratory testing
- Positive and negative test cases
- API testing using Postman
- Browser DevTools inspection

The primary focus was on realistic user workflows and observable application behavior.

Where functionality could not be fully executed because required credentials, payment information, or backend access were unavailable, the corresponding test cases were marked as **NOT EXECUTED** rather than assumed to pass.

## 4. Test Environment

- **Application:** Toolshop — With Bugs
- **Platform:** Web
- **Client:** Desktop browser
- **API Tool:** Postman
- **Browser Tool:** Browser DevTools

## 5. Test Deliverables

The project contains:

- Test Plan
- Test Scenarios
- Test Cases
- Test Execution Results
- Bug Reports
- DevTools Investigations
- Postman API Test Collection
- Final Test Summary

## 6. Risks and Limitations

- Full authentication workflows were not systematically executed.
- Checkout completion was not validated because payment/order completion was outside the current scope.
- Direct database access was unavailable, so database-level validation was not performed.
- Only selected DevTools investigations were conducted.
- Testing was performed in a desktop web environment and does not represent full cross-browser or device coverage.

## 7. Entry Criteria

Testing could begin once:

- The application was accessible.
- Core product catalog functionality was available.
- Browser DevTools was available.
- Postman was available for API testing.

## 8. Exit Criteria

Testing was considered complete for the defined scope when:

- The planned manual test cases were documented.
- Targeted execution was completed where practical.
- Observed defects were documented.
- Selected API endpoints were tested.
- DevTools investigations were documented.
- Overall test findings were summarized.

## 9. Defect Management

Observed defects were documented with:

- Clear reproduction steps
- Expected result
- Actual result
- Severity
- Priority
- Related test cases
- Relevant technical observations where available

Root causes were not assumed when they could not be established from available evidence. 
