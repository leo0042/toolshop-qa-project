# DevTools Investigations

## Investigation 1 — Add-to-Cart Error Behavior

### Objective

Investigate why a "Something went wrong" message appears when adding a product to the cart.

### Actions

- Opened Browser DevTools.
- Enabled Network recording.
- Selected "All" requests.
- Cleared existing entries.
- Performed Add-to-Cart action.

### Observation

- No new visible network request appeared.
- The product was successfully added to the cart.
- The application displayed a "Something went wrong" message.

### Conclusion

The behavior could not be classified as an API/server failure based solely on Network observations.

Further technical investigation would be required to determine the root cause.

Related defect:

- BUG-002 — Add-to-Cart Displays Error Despite Successful Addition

---

## Investigation 2 — Cart Quantity Controls

### Objective

Investigate the cart quantity increase control.

### Actions

- Opened Browser DevTools → Elements.
- Inspected the `+` quantity control.

### Relevant HTML

```html
<button data-test="increase-quantity"
        id="btn-increase-quantity"
        class="btn btn-secondary">
    <i class="fa fa-plus"></i>
</button>
```

### Observation

- The quantity control exists as a valid HTML button.
- The control contains a unique ID.
- The control contains a dedicated testing attribute:
  `data-test="increase-quantity"`.

### Conclusion

The UI control exists and appears correctly implemented visually, but clicking the control does not trigger the expected quantity update behavior.

Related defect:

- BUG-001 — Cart Quantity Controls Are Non-Functional 
