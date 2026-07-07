# KAN-8: Promo Code Validation and Dynamic Cart Discount Calculation

## Test Cases

---

**Test Case ID:** KAN-8-TC-001  
**Preconditions:** User is logged in and has items in the cart  
**Steps:**  
1. Navigate to the cart page  
2. Enter a valid promo code in the promo code field  
3. Click "Apply"  
**Expected Results:**  
- Promo code is accepted  
- Discount is applied to the cart total  
- Discount amount is displayed  
**Negative Scenarios:**  
- Entering an expired or invalid promo code  
- Applying the same promo code twice  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-002  
**Preconditions:** User is on the cart page with items  
**Steps:**  
1. Enter an invalid promo code  
2. Click "Apply"  
**Expected Results:**  
- Error message "Invalid promo code" is displayed  
- No discount is applied  
**Negative Scenarios:**  
- SQL injection attempt in promo code field  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-003  
**Preconditions:** User has a cart total above the minimum required for promo code  
**Steps:**  
1. Enter a promo code with a minimum spend requirement  
2. Click "Apply"  
**Expected Results:**  
- Promo code is accepted  
- Discount is applied  
**Negative Scenarios:**  
- Cart total below minimum requirement  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-004  
**Preconditions:** User has a cart with ineligible items (e.g., excluded from promo)  
**Steps:**  
1. Enter a valid promo code  
2. Click "Apply"  
**Expected Results:**  
- Promo code is rejected for ineligible items  
- Error message specifies ineligible items  
**Negative Scenarios:**  
- All items ineligible  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-005  
**Preconditions:** User has already used the promo code in a previous order  
**Steps:**  
1. Enter the same promo code  
2. Click "Apply"  
**Expected Results:**  
- Error message "Promo code already used"  
- No discount applied  
**Negative Scenarios:**  
- Attempting with multiple accounts  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-006  
**Preconditions:** User is not logged in  
**Steps:**  
1. Add items to cart  
2. Enter a valid promo code  
3. Click "Apply"  
**Expected Results:**  
- Promo code can be applied if allowed for guest users  
- Otherwise, prompt to log in  
**Negative Scenarios:**  
- Guest user restrictions  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-007  
**Preconditions:** User has multiple promo codes  
**Steps:**  
1. Enter first promo code  
2. Click "Apply"  
3. Enter second promo code  
4. Click "Apply"  
**Expected Results:**  
- Only one promo code can be active  
- Error or replacement of previous code  
**Negative Scenarios:**  
- Attempt to stack codes  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-008  
**Preconditions:** Promo code is expired  
**Steps:**  
1. Enter expired promo code  
2. Click "Apply"  
**Expected Results:**  
- Error message "Promo code expired"  
- No discount applied  
**Negative Scenarios:**  
- System clock manipulation  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-009  
**Preconditions:** User applies promo code, then removes an item from cart  
**Steps:**  
1. Apply valid promo code  
2. Remove item(s) from cart  
**Expected Results:**  
- Discount recalculates based on new cart total  
- Promo code is removed if cart no longer qualifies  
**Negative Scenarios:**  
- Cart total drops below minimum  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-010  
**Preconditions:** User applies promo code, then adds more items  
**Steps:**  
1. Apply valid promo code  
2. Add more items to cart  
**Expected Results:**  
- Discount recalculates dynamically  
- Promo code remains valid  
**Negative Scenarios:**  
- Adding ineligible items  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-011  
**Preconditions:** User applies promo code, then updates quantity of items  
**Steps:**  
1. Apply valid promo code  
2. Change quantity of items  
**Expected Results:**  
- Discount recalculates based on new quantity  
**Negative Scenarios:**  
- Quantity change invalidates promo  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-012  
**Preconditions:** User applies promo code, then logs out and logs back in  
**Steps:**  
1. Apply valid promo code  
2. Log out  
3. Log back in  
4. Check cart  
**Expected Results:**  
- Promo code and discount persist if cart is saved  
**Negative Scenarios:**  
- Cart session lost  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-013  
**Preconditions:** User applies promo code, proceeds to checkout  
**Steps:**  
1. Apply valid promo code  
2. Proceed to payment  
**Expected Results:**  
- Discount is reflected in order summary and payment  
**Negative Scenarios:**  
- Discount not reflected at payment  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-014  
**Preconditions:** User applies promo code, then abandons cart  
**Steps:**  
1. Apply valid promo code  
2. Close browser  
3. Reopen and restore cart  
**Expected Results:**  
- Promo code and discount persist if within session  
**Negative Scenarios:**  
- Session timeout  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-015  
**Preconditions:** User applies promo code, then changes shipping address  
**Steps:**  
1. Apply valid promo code  
2. Change shipping address  
**Expected Results:**  
- Discount remains if promo is not location-restricted  
- Error if promo is location-specific  
**Negative Scenarios:**  
- Address outside promo region  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-016  
**Preconditions:** User applies promo code, then changes payment method  
**Steps:**  
1. Apply valid promo code  
2. Change payment method  
**Expected Results:**  
- Discount remains if promo is not payment-method restricted  
- Error if promo is payment-method specific  
**Negative Scenarios:**  
- Payment method not eligible  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-017  
**Preconditions:** User applies promo code, then updates billing information  
**Steps:**  
1. Apply valid promo code  
2. Update billing info  
**Expected Results:**  
- Discount remains  
**Negative Scenarios:**  
- Billing info triggers fraud detection  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-018  
**Preconditions:** User applies promo code, then tries to remove the promo code  
**Steps:**  
1. Apply valid promo code  
2. Click "Remove Promo Code"  
**Expected Results:**  
- Discount is removed  
- Cart total updates  
**Negative Scenarios:**  
- Remove button not working  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-019  
**Preconditions:** User applies promo code, then tries to apply a different promo code  
**Steps:**  
1. Apply first promo code  
2. Apply second promo code  
**Expected Results:**  
- First promo code is replaced by second  
- Discount updates accordingly  
**Negative Scenarios:**  
- Both codes applied simultaneously  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-020  
**Preconditions:** User applies promo code, then network connection is lost  
**Steps:**  
1. Apply valid promo code  
2. Disconnect network  
3. Reconnect and refresh cart  
**Expected Results:**  
- Promo code and discount persist if applied  
- Error if application failed  
**Negative Scenarios:**  
- Data loss, duplicate application  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

*Test cases generated and validated for KAN-8. No PII/PHI/PCI detected. Compliance: ISO27001, SOC2, PCI-DSS, GDPR, SOX. Output structured for QA tool/CI-CD integration.*
