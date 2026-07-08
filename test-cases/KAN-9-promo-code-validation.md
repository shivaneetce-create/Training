# Test Cases for KAN-9: Implement Promo Code Validation and Cart Discount Calculation

---

- **Test Case ID: KAN-9-TC-001**  
  Preconditions:  
    - User has an active shopping cart with at least one item.  
    - Promo code service is available and integrated.  
  Steps:  
    1. Navigate to the cart page.  
    2. Enter a valid, active promo code in the promo code input field.  
    3. Click "Apply".  
  Expected Results:  
    - Promo code is accepted.  
    - Discount is correctly applied to the cart total.  
    - Success message is displayed.  
  Negative Scenarios:  
    - Promo code is expired or inactive.  
    - Promo code is not applicable to items in the cart.  
  Traceability: [KAN-9](https://shivaneeh.atlassian.net/browse/KAN-9)

---

- **Test Case ID: KAN-9-TC-002**  
  Preconditions:  
    - User is on the cart page.  
    - Promo code input field is visible.  
  Steps:  
    1. Enter an invalid promo code (random string).  
    2. Click "Apply".  
  Expected Results:  
    - Error message is displayed: "Invalid promo code".  
    - No discount is applied.  
  Negative Scenarios:  
    - Input contains special characters or SQL injection attempts.  
  Traceability: [KAN-9](https://shivaneeh.atlassian.net/browse/KAN-9)

---

- **Test Case ID: KAN-9-TC-003**  
  Preconditions:  
    - User has a cart with items not eligible for promo code discounts.  
    - Promo code is valid but restricted to certain products.  
  Steps:  
    1. Enter a valid promo code.  
    2. Click "Apply".  
  Expected Results:  
    - Error or info message: "Promo code not applicable to selected items".  
    - No discount applied.  
  Negative Scenarios:  
    - Cart contains both eligible and ineligible items.  
  Traceability: [KAN-9](https://shivaneeh.atlassian.net/browse/KAN-9)

---

- **Test Case ID: KAN-9-TC-004**  
  Preconditions:  
    - User has a cart with multiple eligible items.  
    - Promo code offers a percentage discount.  
  Steps:  
    1. Enter the promo code.  
    2. Click "Apply".  
  Expected Results:  
    - Discount is calculated as a percentage of eligible items’ subtotal.  
    - Cart total is updated accordingly.  
  Negative Scenarios:  
    - Rounding errors in discount calculation.  
  Traceability: [KAN-9](https://shivaneeh.atlassian.net/browse/KAN-9)

---

- **Test Case ID: KAN-9-TC-005**  
  Preconditions:  
    - User has a cart with items.  
    - Promo code has a minimum purchase requirement.  
  Steps:  
    1. Enter the promo code with cart total below the minimum threshold.  
    2. Click "Apply".  
  Expected Results:  
    - Error message: "Minimum purchase amount not met".  
    - No discount applied.  
  Negative Scenarios:  
    - Cart total exactly at the threshold.  
  Traceability: [KAN-9](https://shivaneeh.atlassian.net/browse/KAN-9)

---

- **Test Case ID: KAN-9-TC-006**  
  Preconditions:  
    - User has a cart with items.  
    - Promo code is valid but has a usage limit per user.  
  Steps:  
    1. Apply the promo code once (success).  
    2. Remove items, add new items, and try to apply the same code again.  
  Expected Results:  
    - Error message: "Promo code usage limit reached".  
    - No additional discount applied.  
  Negative Scenarios:  
    - Attempting to bypass limit by logging out/in.  
  Traceability: [KAN-9](https://shivaneeh.atlassian.net/browse/KAN-9)

---

- **Test Case ID: KAN-9-TC-007**  
  Preconditions:  
    - User has a cart with items.  
    - Promo code is expired.  
  Steps:  
    1. Enter the expired promo code.  
    2. Click "Apply".  
  Expected Results:  
    - Error message: "Promo code expired".  
    - No discount applied.  
  Negative Scenarios:  
    - System clock manipulation.  
  Traceability: [KAN-9](https://shivaneeh.atlassian.net/browse/KAN-9)

---

- **Test Case ID: KAN-9-TC-008**  
  Preconditions:  
    - User has a cart with items.  
    - Promo code is valid and active.  
  Steps:  
    1. Apply the promo code.  
    2. Remove an item from the cart.  
    3. Observe if the discount recalculates correctly.  
  Expected Results:  
    - Discount is updated based on new cart contents.  
    - If cart no longer meets requirements, discount is removed and user is notified.  
  Negative Scenarios:  
    - Discount remains after cart becomes ineligible.  
  Traceability: [KAN-9](https://shivaneeh.atlassian.net/browse/KAN-9)

---

- **Test Case ID: KAN-9-TC-009**  
  Preconditions:  
    - User has a cart with items.  
    - Promo code is valid.  
  Steps:  
    1. Apply the promo code.  
    2. Proceed to checkout.  
    3. Complete the purchase.  
  Expected Results:  
    - Discount is reflected in the final order summary and confirmation.  
    - No discrepancies in charged amount.  
  Negative Scenarios:  
    - Discount disappears at checkout.  
  Traceability: [KAN-9](https://shivaneeh.atlassian.net/browse/KAN-9)

---

- **Test Case ID: KAN-9-TC-010**  
  Preconditions:  
    - User has a cart with items.  
    - Promo code input field is present.  
  Steps:  
    1. Enter a promo code with leading/trailing spaces.  
    2. Click "Apply".  
  Expected Results:  
    - System trims spaces and processes the code correctly.  
    - Discount is applied if code is valid.  
  Negative Scenarios:  
    - System fails to trim spaces, resulting in "Invalid code" error.  
  Traceability: [KAN-9](https://shivaneeh.atlassian.net/browse/KAN-9)

---

- **Test Case ID: KAN-9-TC-011**  
  Preconditions:  
    - User has a cart with items.  
    - Promo code is valid for a specific user segment (e.g., new users).  
  Steps:  
    1. Log in as a user not eligible for the promo code.  
    2. Enter the promo code and click "Apply".  
  Expected Results:  
    - Error message: "Promo code not available for your account".  
    - No discount applied.  
  Negative Scenarios:  
    - User segment misclassification.  
  Traceability: [KAN-9](https://shivaneeh.atlassian.net/browse/KAN-9)

---

- **Test Case ID: KAN-9-TC-012**  
  Preconditions:  
    - User has a cart with items.  
    - Promo code input field is present.  
  Steps:  
    1. Enter a promo code containing special characters or script tags.  
    2. Click "Apply".  
  Expected Results:  
    - System sanitizes input and prevents code injection.  
    - Error message for invalid code format.  
  Negative Scenarios:  
    - Application accepts and processes malicious input.  
  Traceability: [KAN-9](https://shivaneeh.atlassian.net/browse/KAN-9)

---

**Audit Log:**  
- [2024-12-19T14:30:00Z] Action: Test cases generated for KAN-9.  
- Sensitive information filtered per compliance policy.  
- All actions logged for audit and traceability.

**Output is structured for direct integration with QA tools and CI/CD pipelines.**
