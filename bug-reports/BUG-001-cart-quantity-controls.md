# BUG-001 — Cart Controls Do Not Modify Cart Contents

## Summary

The primary cart controls for increasing, decreasing, and removing a product do not perform their expected actions.

## Environment

- Application: Toolshop — With Bugs
- Platform: Web
- Browser: Desktop browser
- Area: Shopping Cart
- Severity: Medium
- Priority: High
- Status: Open

## Preconditions

A product has been successfully added to the shopping cart.

## Steps to Reproduce

### Increase Quantity

1. Open the shopping cart.
2. Locate a product in the cart.
3. Click the `+` quantity control.
4. Observe the quantity.

### Decrease Quantity

5. Click the `−` quantity control.
6. Observe the quantity.

### Remove Product

7. Click the `X` remove control.
8. Observe the cart.

## Expected Result

- `+` increases the product quantity.
- `−` decreases the product quantity.
- `X` removes the product from the cart.
- The cart state and total update accordingly.

## Actual Result

- Clicking `+` produces no change.
- Clicking `−` produces no change.
- Clicking `X` does not remove the product.

Manual quantity entry remains functional.

## Reproducibility

Consistently reproduced during exploratory testing.

## Workaround

Product quantity can be changed manually through the quantity field.

No identified workaround was found for removing the product through the cart's remove control.

## Related Test Cases

- TC-17 — Increase product quantity using `+`
- TC-18 — Decrease product quantity using `−`
- TC-20 — Remove a product from the cart

## Impact

Users cannot reliably manage cart contents through the primary controls. This can prevent users from adjusting quantities or removing unwanted products using the expected interface.

## DevTools Investigation

The increase control was inspected and found to be a button containing:

`data-test="increase-quantity"`

`id="btn-increase-quantity"`

The remove control was inspected and found to be an anchor element containing the remove icon:

`class="btn btn-danger"`

The presence of these UI controls was confirmed, but their expected actions did not occur when clicked.

## Evidence

Behavior was observed during manual testing of the Toolshop application.