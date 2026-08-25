# BUG-002 — Add-to-Cart Displays Error Despite Successful Addition

## Summary

Adding a product to the shopping cart displays a "Something went wrong" error message even though the product is successfully added to the cart.

## Environment

- Application: Toolshop — With Bugs
- Platform: Web
- Browser: Desktop browser
- Area: Product Catalog / Shopping Cart
- Severity: Medium
- Priority: High
- Status: Open

## Preconditions

A product is available in the product catalog.

## Steps to Reproduce

1. Open the product catalog.
2. Select an available product.
3. Add the product to the cart.
4. Observe the application response.
5. Open the shopping cart and verify the product.

## Expected Result

The product should be added to the cart successfully and the user should receive an appropriate success indication.

No error message should be displayed when the operation succeeds.

## Actual Result

The product is added successfully to the cart, but the application simultaneously displays a "Something went wrong" message.

## Reproducibility

Observed during manual testing.

## Related Test Case

- TC-15 — Add an available product to the cart

## Impact

The contradictory feedback may cause users to believe that the add-to-cart operation failed even though the product was added successfully. This can lead to repeated actions and confusion about the current cart state.

## Technical Investigation

Browser DevTools Network monitoring was enabled during investigation.

No new visible network request was observed when the add-to-cart action was performed with the Network panel configured to display all requests.

The product was nevertheless added to the cart.

The root cause was not determined during this investigation.

## Evidence

Behavior was observed during manual testing of the Toolshop application. 
