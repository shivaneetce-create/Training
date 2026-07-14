# Test Cases for Story: Implement Promo Code Validation and Dynamic Cart Discount Calculation

## Issue Key: KAN-9

### Traceability: https://jira.example.com/browse/KAN-9

---

**Test Case ID: KAN-9-TC-001**
- Preconditions: User is logged in and has items in the cart
- Steps:
  1. Navigate to the cart page
  2. Enter a valid promo code
  3. Click 'Apply'
- Expected Results: Discount is applied to the cart total, and the promo code is marked as applied
- Negative Scenarios: Entering an expired or invalid promo code

**Test Case ID: KAN-9-TC-002**
- Preconditions: User is logged in with an empty cart
- Steps:
  1. Navigate to the cart page
  2. Enter a valid promo code
  3. Click 'Apply'
- Expected Results: System displays a message indicating promo codes cannot be applied to empty carts
- Negative Scenarios: Attempting to proceed to checkout with an empty cart

**Test Case ID: KAN-9-TC-003**
- Preconditions: User is logged in with items in the cart
- Steps:
  1. Enter an invalid promo code
  2. Click 'Apply'
- Expected Results: System displays an error message indicating the promo code is invalid
- Negative Scenarios: Entering a code with special characters

**Test Case ID: KAN-9-TC-004**
- Preconditions: User is logged in with items in the cart
- Steps:
  1. Enter an expired promo code
  2. Click 'Apply'
- Expected Results: System displays an error message indicating the promo code is expired
- Negative Scenarios: Entering a code with a past expiration date

**Test Case ID: KAN-9-TC-005**
- Preconditions: User is logged in with items in the cart
- Steps:
  1. Enter a promo code that has already been used
  2. Click 'Apply'
- Expected Results: System displays an error message indicating the promo code has already been used
- Negative Scenarios: Reusing a single-use promo code

**Test Case ID: KAN-9-TC-006**
- Preconditions: User is logged in with items in the cart
- Steps:
  1. Enter a promo code with minimum cart value requirement
  2. Ensure cart value is below the minimum
  3. Click 'Apply'
- Expected Results: System displays a message indicating the minimum cart value is not met
- Negative Scenarios: Cart value just below the threshold

**Test Case ID: KAN-9-TC-007**
- Preconditions: User is logged in with items in the cart
- Steps:
  1. Enter a promo code with a maximum discount cap
  2. Ensure cart value is high enough to exceed the cap
  3. Click 'Apply'
- Expected Results: Discount applied does not exceed the maximum cap
- Negative Scenarios: Cart value extremely high

**Test Case ID: KAN-9-TC-008**
- Preconditions: User is logged in with items in the cart
- Steps:
  1. Enter a promo code restricted to specific products
  2. Ensure cart contains both eligible and ineligible products
  3. Click 'Apply'
- Expected Results: Discount is applied only to eligible products
- Negative Scenarios: All products ineligible

**Test Case ID: KAN-9-TC-009**
- Preconditions: User is logged in with items in the cart
- Steps:
  1. Enter a promo code restricted to first-time users
  2. User is not a first-time user
  3. Click 'Apply'
- Expected Results: System displays a message indicating the promo code is not valid for this user
- Negative Scenarios: User with multiple accounts

**Test Case ID: KAN-9-TC-010**
- Preconditions: User is logged in with items in the cart
- Steps:
  1. Enter a promo code
  2. Remove an item from the cart
  3. Observe discount recalculation
- Expected Results: Discount is dynamically recalculated based on the new cart contents
- Negative Scenarios: Removing all eligible items

**Test Case ID: KAN-9-TC-011**
- Preconditions: User is logged in with items in the cart
- Steps:
  1. Enter a promo code
  2. Add more items to the cart
  3. Observe discount recalculation
- Expected Results: Discount is dynamically recalculated based on the updated cart contents
- Negative Scenarios: Adding ineligible items

**Test Case ID: KAN-9-TC-012**
- Preconditions: User is logged in with items in the cart
- Steps:
  1. Enter a promo code
  2. Proceed to checkout
  3. Complete the purchase
- Expected Results: Discount is reflected in the final order summary and invoice
- Negative Scenarios: Discount not reflected at checkout

**Test Case ID: KAN-9-TC-013**
- Preconditions: User is logged in with items in the cart
- Steps:
  1. Enter a promo code
  2. Click 'Remove' on the applied promo code
- Expected Results: Discount is removed and cart total is updated
- Negative Scenarios: Removing promo code after checkout

**Test Case ID: KAN-9-TC-014**
- Preconditions: User is logged in with items in the cart
- Steps:
  1. Enter a promo code
  2. Refresh the cart page
- Expected Results: Promo code and discount persist after page reload
- Negative Scenarios: Session timeout

**Test Case ID: KAN-9-TC-015**
- Preconditions: User is logged in with items in the cart
- Steps:
  1. Enter a promo code
  2. Log out and log back in
  3. Navigate to cart
- Expected Results: Promo code and discount persist for the session
- Negative Scenarios: Promo code lost after logout

**Test Case ID: KAN-9-TC-016**
- Preconditions: User is logged in with items in the cart
- Steps:
  1. Enter a promo code
  2. Open cart in a new browser tab
- Expected Results: Promo code and discount are consistent across tabs
- Negative Scenarios: Inconsistent state between tabs

**Test Case ID: KAN-9-TC-017**
- Preconditions: User is logged in with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply a second promo code
- Expected Results: System allows only one promo code at a time
- Negative Scenarios: Multiple promo codes applied

**Test Case ID: KAN-9-TC-018**
- Preconditions: User is logged in with items in the cart
- Steps:
  1. Enter a promo code
  2. Change the quantity of an item
  3. Observe discount recalculation
- Expected Results: Discount is dynamically recalculated based on new quantities
- Negative Scenarios: Quantity set to zero

**Test Case ID: KAN-9-TC-019**
- Preconditions: User is logged in with items in the cart
- Steps:
  1. Enter a promo code
  2. Cart value drops below minimum after item removal
  3. Observe discount removal
- Expected Results: Discount is removed and user is notified
- Negative Scenarios: No notification shown

**Test Case ID: KAN-9-TC-020**
- Preconditions: User is logged in with items in the cart
- Steps:
  1. Enter a promo code
  2. Cart value increases above minimum after adding items
  3. Observe discount application
- Expected Results: Discount is applied once minimum is met
- Negative Scenarios: Discount not applied after threshold met

**Test Case ID: KAN-9-TC-021**
- Preconditions: User is logged in with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply the same promo code on another account
- Expected Results: System enforces usage limits per user/account
- Negative Scenarios: Promo code used across multiple accounts

**Test Case ID: KAN-9-TC-022**
- Preconditions: User is logged in with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply a promo code with whitespace
- Expected Results: System trims whitespace and validates code
- Negative Scenarios: Code rejected due to whitespace

**Test Case ID: KAN-9-TC-023**
- Preconditions: User is logged in with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply a promo code with case differences (e.g., lower/upper case)
- Expected Results: System treats promo codes as case-insensitive
- Negative Scenarios: Code rejected due to case sensitivity

**Test Case ID: KAN-9-TC-024**
- Preconditions: User is logged in with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply a promo code with special characters
- Expected Results: System validates and rejects codes with invalid characters
- Negative Scenarios: Code accepted with invalid characters

**Test Case ID: KAN-9-TC-025**
- Preconditions: User is logged in with items in the cart
- Steps:
  1. Enter a promo code
  2. Network connection is lost before applying
  3. Restore connection and retry
- Expected Results: System handles network errors gracefully and allows retry
- Negative Scenarios: Promo code lost or applied incorrectly after reconnect

---

Audit Log:
- Fetched issue KAN-9 from Jira.
- Verified status is "Ready".
- Generated 25 detailed test cases with preconditions, steps, expected results, negative scenarios, and traceability.
- Filtered output for sensitive information (no PII or confidential data present).
- Structured output for QA tool and CI/CD integration.

End of output.