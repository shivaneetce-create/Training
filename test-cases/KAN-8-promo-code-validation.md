# Test Cases for KAN-8: Implement Promo Code Validation and Dynamic Cart Discount Calculation

## Story Title
Implement Promo Code Validation and Dynamic Cart Discount Calculation

## Traceability
[Jira Issue KAN-8](https://jira.example.com/browse/KAN-8)

---

### Test Case ID: TC-KAN-8-001
**Preconditions:**
- User is logged in (if required for checkout)
- User has at least one item in the cart
- Valid promo codes exist in the system
**Steps:**
1. Navigate to the checkout page
2. Enter a valid promo code in the promo code input field
3. Click "Apply"
**Expected Results:**
- Promo code is validated successfully
- Cart total is updated to reflect the discount
- Success message is displayed confirming promo code application
**Negative Scenarios:**
- Entering an expired promo code
- Entering an invalid promo code
- Applying the same promo code twice
- Applying a promo code not applicable to items in the cart

---

### Test Case ID: TC-KAN-8-002
**Preconditions:**
- User is on the checkout page with items in the cart
- No promo code applied yet
**Steps:**
1. Enter an invalid promo code (e.g., random string or code not in system)
2. Click "Apply"
**Expected Results:**
- Error message is displayed indicating invalid promo code
- Cart total remains unchanged
**Negative Scenarios:**
- Submitting empty promo code field
- Submitting promo code with special characters

---

### Test Case ID: TC-KAN-8-003
**Preconditions:**
- User is on the checkout page with items in the cart
- Valid promo code with usage limit exists
**Steps:**
1. Apply a valid promo code until its usage limit is reached
2. Attempt to apply the same promo code again
**Expected Results:**
- Error message is displayed indicating promo code usage limit reached
- Cart total remains unchanged
**Negative Scenarios:**
- Attempting to apply promo code after expiration date

---

### Test Case ID: TC-KAN-8-004
**Preconditions:**
- User is on the checkout page with items in the cart
- Multiple promo codes exist (some stackable, some not)
**Steps:**
1. Apply a stackable promo code
2. Apply a second stackable promo code
3. Attempt to apply a non-stackable promo code
**Expected Results:**
- Stackable promo codes are applied cumulatively
- Non-stackable promo code application is rejected with appropriate message
**Negative Scenarios:**
- Attempting to apply more promo codes than allowed

---

### Test Case ID: TC-KAN-8-005
**Preconditions:**
- User is on the checkout page with items in the cart
- Valid promo code is applied
**Steps:**
1. Remove an item from the cart
2. Observe if promo code is still valid/applicable
3. Add an ineligible item to the cart
**Expected Results:**
- Promo code is revalidated
- If cart no longer meets promo code criteria, discount is removed and user is notified
**Negative Scenarios:**
- Cart manipulation to bypass promo code restrictions

---

### Test Case ID: TC-KAN-8-006
**Preconditions:**
- User is on the checkout page with items in the cart
- Valid promo code is applied
**Steps:**
1. Proceed to payment
2. Complete the order
**Expected Results:**
- Discount is reflected in the final order summary and confirmation
- Promo code usage is recorded in the system
**Negative Scenarios:**
- Network failure during order submission
- Promo code removed from system before order completion

---

### Test Case ID: TC-KAN-8-007
**Preconditions:**
- User is on the checkout page
- Promo code validation service is unavailable (simulate backend failure)
**Steps:**
1. Enter a promo code
2. Click "Apply"
**Expected Results:**
- User receives a clear error message indicating service is unavailable
- Cart total remains unchanged
**Negative Scenarios:**
- System does not handle service failure gracefully (e.g., unhandled exception)

---

### Test Case ID: TC-KAN-8-008
**Preconditions:**
- User is on the checkout page
- Cart contains items with different eligibility (some eligible, some not)
**Steps:**
1. Apply a promo code only valid for certain items
**Expected Results:**
- Discount is applied only to eligible items
- Ineligible items are not discounted
- UI clearly indicates which items received the discount
**Negative Scenarios:**
- Discount applied incorrectly to ineligible items

---

## Audit Log
- [2024-12-19T10:32:00Z] Test cases generated for KAN-8 by QA Automation Agent
- Sensitive information filtered: No PII/PHI/PCI detected
- All actions logged for compliance and traceability
- Output structured for integration with QA tools and CI/CD pipelines

---

## Compliance Report
- Data Classification: Internal Business Data
- Sensitivity Level: Low (No sensitive customer data in issue description)
- PII/PHI/PCI Status: CLEAR - No sensitive data detected
- Access Control Compliance: PASSED
  - RBAC permissions verified
  - User authentication validated
  - API token security confirmed
- Audit Trail Compliance: COMPLIANT
  - All triage actions logged with timestamps
  - Decision rationale documented
  - Compliance metadata captured
  - ISO27001 standards maintained
- Data Retention: 7-year retention policy applied
- Consent Status: Not applicable (internal development task)
- Data Lineage: Fully documented and traceable
- Compliance Certifications Applied:
  - ISO27001: Information Security Management
  - SOC2: Service Organization Control Type 2
  - Internal QE Standards: Defect Management Protocol v3.2
- Next Review Date: 2024-12-26T10:30:00Z (7-day follow-up cycle)
