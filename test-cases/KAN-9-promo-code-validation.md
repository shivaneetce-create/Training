# Test Cases for Story: Implement Promo Code Validation and Dynamic Cart Discount Calculation

---

## Test Case ID: TC-KAN-9-001
- Preconditions: User is logged in and has items in the cart; promo code exists and is valid.
- Steps:
  1. Navigate to cart page.
  2. Enter a valid promo code in the promo code input field.
  3. Click "Apply".
- Expected Results: Promo code is validated; cart discount is applied; cart total is updated accordingly.
- Negative Scenarios: Entering an expired or invalid promo code.
- Traceability: https://jira.example.com/browse/KAN-9

---

## Test Case ID: TC-KAN-9-002
- Preconditions: User is logged in; cart contains items; promo code is invalid.
- Steps:
  1. Navigate to cart page.
  2. Enter an invalid promo code.
  3. Click "Apply".
- Expected Results: Error message is displayed; no discount is applied; cart total remains unchanged.
- Negative Scenarios: Entering a promo code with special characters or blank input.
- Traceability: https://jira.example.com/browse/KAN-9

---

## Test Case ID: TC-KAN-9-003
- Preconditions: User is logged in; cart contains items; promo code is expired.
- Steps:
  1. Navigate to cart page.
  2. Enter an expired promo code.
  3. Click "Apply".
- Expected Results: Error message indicating promo code is expired; no discount applied.
- Negative Scenarios: Entering a promo code with future activation date.
- Traceability: https://jira.example.com/browse/KAN-9

---

## Test Case ID: TC-KAN-9-004
- Preconditions: User is logged in; cart contains items; promo code is valid for specific products.
- Steps:
  1. Add eligible and non-eligible products to cart.
  2. Enter valid promo code.
  3. Click "Apply".
- Expected Results: Discount is applied only to eligible products; cart total reflects partial discount.
- Negative Scenarios: Applying promo code to cart with only non-eligible products.
- Traceability: https://jira.example.com/browse/KAN-9

---

## Test Case ID: TC-KAN-9-005
- Preconditions: User is logged in; cart contains items; promo code has usage limit.
- Steps:
  1. Enter promo code that has reached its usage limit.
  2. Click "Apply".
- Expected Results: Error message indicating promo code usage limit reached; no discount applied.
- Negative Scenarios: Multiple users attempting to use the same code simultaneously.
- Traceability: https://jira.example.com/browse/KAN-9

---

## Test Case ID: TC-KAN-9-006
- Preconditions: User is logged in; cart contains items; promo code is valid; cart total meets minimum spend requirement.
- Steps:
  1. Add items to cart to meet minimum spend.
  2. Enter valid promo code.
  3. Click "Apply".
- Expected Results: Discount is applied; cart total is updated.
- Negative Scenarios: Cart total below minimum spend requirement.
- Traceability: https://jira.example.com/browse/KAN-9

---

## Test Case ID: TC-KAN-9-007
- Preconditions: User is logged in; cart contains items; promo code is valid; cart total exceeds maximum discount cap.
- Steps:
  1. Add items to cart to exceed maximum discount cap.
  2. Enter valid promo code.
  3. Click "Apply".
- Expected Results: Discount applied up to maximum cap; cart total reflects capped discount.
- Negative Scenarios: Cart total exactly at cap threshold.
- Traceability: https://jira.example.com/browse/KAN-9

---

## Test Case ID: TC-KAN-9-008
- Preconditions: User is logged in; cart contains items; promo code is valid; user removes items after applying promo code.
- Steps:
  1. Apply valid promo code.
  2. Remove items from cart.
- Expected Results: Discount recalculates dynamically; cart total updates; promo code may be invalidated if requirements are no longer met.
- Negative Scenarios: Removing all items from cart after applying promo code.
- Traceability: https://jira.example.com/browse/KAN-9

---

## Test Case ID: TC-KAN-9-009
- Preconditions: User is logged in; cart contains items; promo code is valid; user updates quantity of items after applying promo code.
- Steps:
  1. Apply valid promo code.
  2. Change item quantities in cart.
- Expected Results: Discount recalculates dynamically; cart total updates accordingly.
- Negative Scenarios: Changing quantity to zero for all items.
- Traceability: https://jira.example.com/browse/KAN-9

---

## Test Case ID: TC-KAN-9-010
- Preconditions: User is logged in; cart contains items; promo code is valid; user proceeds to checkout.
- Steps:
  1. Apply valid promo code.
  2. Proceed to checkout.
  3. Complete payment.
- Expected Results: Discount is reflected in final payment; promo code is marked as used if single-use.
- Negative Scenarios: Payment fails after promo code applied.
- Traceability: https://jira.example.com/browse/KAN-9

---

Audit Log:
- Fetched story title and status from Jira: KAN-9, status "Ready".
- Generated 10 detailed test cases with preconditions, steps, expected results, negative scenarios, and traceability links.
- Filtered output for sensitive information (no sensitive data present).
- Structured output for QA tool and CI/CD integration.

End of output.
