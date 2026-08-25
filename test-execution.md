# Toolshop — Test Execution Results

## Execution Information

- **Application:** Toolshop — With Bugs
- **Test Type:** Manual Functional Testing
- **Environment:** Web browser / Desktop
- **Execution Status:** Partial execution with targeted exploratory validation
- **Execution Focus:** Authentication, product catalog, shopping cart, and checkout behavior

## Results

| ID | Test Case | Result | Notes |
|---|---|---|---|
| TC-01 | Register with valid required information | NOT EXECUTED | Registration form and required fields were observed; full registration flow not executed |
| TC-02 | Register with an already-registered email | NOT EXECUTED | Negative registration behavior not executed |
| TC-03 | Login with valid credentials | NOT EXECUTED | Full authentication flow not executed |
| TC-04 | Login with an incorrect password | NOT EXECUTED | Negative login behavior not executed |
| TC-05 | Login with an unregistered email | NOT EXECUTED | Negative login behavior not executed |
| TC-06 | Logout from an authenticated session | NOT EXECUTED | Requires completed authentication flow |
| TC-07 | Open the product catalog | PASS | Product catalog loaded and products were displayed |
| TC-08 | Search using an existing product name | PASS | Search functionality was observed working during exploratory testing |
| TC-09 | Search using a partial product name | NOT EXECUTED | Not specifically validated |
| TC-10 | Search for a non-existent product | NOT EXECUTED | Not specifically validated |
| TC-11 | Apply a product category filter | PASS | Category filtering was observed working |
| TC-12 | Change or remove an applied filter | NOT EXECUTED | Not specifically validated |
| TC-13 | Open a product from the catalog | PASS | Product details opened correctly |
| TC-14 | Verify product information | PASS | Product information appeared correctly for products checked |
| TC-15 | Add an available product to the cart | FAIL | Product was added, but an unexpected "Something went wrong" message was displayed |
| TC-16 | Add multiple different products to the cart | NOT EXECUTED | Not specifically validated |
| TC-17 | Increase product quantity using the `+` control | FAIL | Clicking `+` produced no change |
| TC-18 | Decrease product quantity using the `−` control | FAIL | Clicking `−` produced no change |
| TC-19 | Manually change the product quantity | PASS | Manual quantity entry changed the quantity |
| TC-20 | Remove a product from the cart | FAIL | Not specifically validated |
| TC-21 | Verify cart total calculation | NOT EXECUTED | Not specifically validated |
| TC-22 | Attempt checkout with required information missing/invalid | NOT EXECUTED | Checkout flow was reached but validation was not systematically executed |
| TC-23 | Complete checkout with valid test information | NOT EXECUTED | Not executed; payment/order completion was not required for the current scope |

## Defects Identified

### BUG-001 — Cart quantity controls are non-functional

**Related test cases:** TC-17, TC-18

The `+` and `−` controls did not change the product quantity when clicked. Manual quantity entry remained functional.

### BUG-002 — Add-to-cart displays an error after successful addition

**Related test case:** TC-15

A product was successfully added to the cart, but the application displayed a "Something went wrong" message immediately after the action.

This behavior requires further investigation before final defect classification.

## DevTools Observation

During investigation of the add-to-cart behavior:

- Browser DevTools Network recording was enabled.
- The Network panel was checked with **All** requests selected.
- No new visible network request appeared when the product was added to the cart.
- The product was nevertheless added successfully.

Therefore, the observation was not classified as an API/server failure based solely on Network activity.. 
