# Test Cases for Story: Implement Promo Code Validation and Dynamic Cart Discount Calculation (KAN-9)

## Test Case ID: TC-KAN-9-001
**Preconditions:** User is logged in and has items in the cart
**Steps:**
  1. Navigate to the cart page
  2. Enter a valid promo code in the promo code field
  3. Click 'Apply'
**Expected Results:**
  - Promo code is validated successfully
  - Discount is applied to the cart total dynamically
**Negative Scenarios:**
  - Promo code expired
  - Promo code not applicable to cart items
**Traceability:** https://jira.example.com/browse/KAN-9

## Test Case ID: TC-KAN-9-002
**Preconditions:** User is logged in, cart contains eligible items
**Steps:**
  1. Enter an invalid promo code
  2. Click 'Apply'
**Expected Results:**
  - Error message displayed: "Invalid promo code"
  - No discount applied
**Negative Scenarios:**
  - Typo in promo code
  - Promo code format incorrect
**Traceability:** https://jira.example.com/browse/KAN-9

## Test Case ID: TC-KAN-9-003
**Preconditions:** User is logged in, cart contains items, promo code has usage limit
**Steps:**
  1. Enter a promo code that has reached its usage limit
  2. Click 'Apply'
**Expected Results:**
  - Error message: "Promo code usage limit reached"
  - No discount applied
**Negative Scenarios:**
  - Multiple users using the same code simultaneously
**Traceability:** https://jira.example.com/browse/KAN-9

## Test Case ID: TC-KAN-9-004
**Preconditions:** User is logged in, cart contains items, promo code is valid for specific products
**Steps:**
  1. Add ineligible items to cart
  2. Enter valid promo code
  3. Click 'Apply'
**Expected Results:**
  - Error message: "Promo code not applicable to selected items"
  - No discount applied
**Negative Scenarios:**
  - Mixed eligible and ineligible items
**Traceability:** https://jira.example.com/browse/KAN-9

## Test Case ID: TC-KAN-9-005
**Preconditions:** User is logged in, cart contains items, promo code is valid
**Steps:**
  1. Apply promo code
  2. Remove an item from cart
  3. Observe cart total and discount
**Expected Results:**
  - Discount recalculates dynamically based on updated cart contents
**Negative Scenarios:**
  - Removing all eligible items removes discount
**Traceability:** https://jira.example.com/browse/KAN-9

## Test Case ID: TC-KAN-9-006
**Preconditions:** User is logged in, cart contains items, promo code is valid
**Steps:**
  1. Apply promo code
  2. Add more eligible items to cart
  3. Observe cart total and discount
**Expected Results:**
  - Discount recalculates dynamically based on new cart contents
**Negative Scenarios:**
  - Adding ineligible items does not increase discount
**Traceability:** https://jira.example.com/browse/KAN-9

## Test Case ID: TC-KAN-9-007
**Preconditions:** User is logged in, cart contains items, promo code is valid
**Steps:**
  1. Apply promo code
  2. Proceed to checkout
  3. Complete payment
**Expected Results:**
  - Discount is reflected in final payment amount
  - Promo code is marked as used if single-use
**Negative Scenarios:**
  - Payment fails, promo code remains unused
**Traceability:** https://jira.example.com/browse/KAN-9

## Test Case ID: TC-KAN-9-008
**Preconditions:** User is logged in, cart contains items, promo code is valid
**Steps:**
  1. Apply promo code
  2. Refresh cart page
  3. Verify discount persists
**Expected Results:**
  - Discount remains applied after page refresh
**Negative Scenarios:**
  - Session timeout removes discount
**Traceability:** https://jira.example.com/browse/KAN-9

## Test Case ID: TC-KAN-9-009
**Preconditions:** User is logged in, cart contains items, promo code is valid
**Steps:**
  1. Apply promo code
  2. Log out and log back in
  3. Navigate to cart
**Expected Results:**
  - Discount remains applied if cart is persistent
**Negative Scenarios:**
  - Cart is cleared, discount lost
**Traceability:** https://jira.example.com/browse/KAN-9

## Test Case ID: TC-KAN-9-010
**Preconditions:** User is logged in, cart contains items, promo code is valid
**Steps:**
  1. Apply promo code
  2. Attempt to apply a second promo code
**Expected Results:**
  - Error message: "Only one promo code can be applied"
  - No additional discount applied
**Negative Scenarios:**
  - Multiple promo codes allowed erroneously
**Traceability:** https://jira.example.com/browse/KAN-9

---

**Audit Log:**
- Fetched issue details for KAN-9 from Jira
- Status verified as "Ready"
- Generated 10 detailed test cases with preconditions, steps, expected results, negative scenarios, and traceability links
- Sensitive information filtered (no user data, no attachments, no comments)
- Output structured for QA tool and CI/CD integration
