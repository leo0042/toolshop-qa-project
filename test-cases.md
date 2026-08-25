# Toolshop — Test Cases

## Authentication

| ID | Test Case | Expected Result |
|---|---|---|
| TC-01 | Register with valid required information | A new user account is created successfully |
| TC-02 | Register with an already-registered email | Registration is rejected with appropriate validation feedback |
| TC-03 | Login with valid credentials | User is authenticated successfully |
| TC-04 | Login with an incorrect password | Login is rejected and appropriate feedback is displayed |
| TC-05 | Login with an unregistered email | Login is rejected and appropriate feedback is displayed |
| TC-06 | Logout from an authenticated session | User is logged out and authenticated state is cleared |

## Product Catalog

| ID | Test Case | Expected Result |
|---|---|---|
| TC-07 | Open the product catalog | Available products are displayed correctly |
| TC-08 | Search using an existing product name | Relevant matching products are displayed |
| TC-09 | Search using a partial product name | Products matching the search term are displayed |
| TC-10 | Search for a non-existent product | No matching products or an appropriate empty state is displayed |
| TC-11 | Apply a product category filter | Only products matching the selected category are displayed |
| TC-12 | Change or remove an applied filter | Product results update correctly |
| TC-13 | Open a product from the catalog | Correct product details are displayed |
| TC-14 | Verify product information | Product name, price, description, image, and availability are displayed consistently |

## Shopping Cart

| ID | Test Case | Expected Result |
|---|---|---|
| TC-15 | Add an available product to the cart | Product is added with the correct quantity and price |
| TC-16 | Add multiple different products to the cart | All selected products are displayed correctly |
| TC-17 | Increase product quantity using the `+` control | Quantity increases and the cart total updates accordingly |
| TC-18 | Decrease product quantity using the `−` control | Quantity decreases and the cart total updates accordingly |
| TC-19 | Manually change the product quantity | Quantity and cart total update according to the entered value |
| TC-20 | Remove a product from the cart | Product is removed and the cart total updates |
| TC-21 | Verify cart total calculation | Cart total equals the sum of product price × quantity |

## Checkout

| ID | Test Case | Expected Result |
|---|---|---|
| TC-22 | Attempt checkout with required information missing/invalid | Appropriate validation feedback is displayed and checkout cannot proceed |
| TC-23 | Complete checkout with valid test information where safely supported | Order is successfully submitted and appropriate confirmation/order information is displayed |. 
