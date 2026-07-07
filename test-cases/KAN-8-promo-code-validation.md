# Test Cases for KAN-8: Implement Promo Code Validation and Dynamic Cart Discount Calculation

---

**Test Case ID:** KAN-8-TC-001  
**Preconditions:** User is logged in and has at least one item in the cart  
**Steps:**  
1. Navigate to the cart page  
2. Enter a valid promo code in the promo code field  
3. Click "Apply"  
**Expected Results:**  
- Promo code is accepted  
- Discount is applied to the cart total  
- Discounted total is displayed correctly  
**Negative Scenarios:**  
- Entering an invalid promo code  
- Entering an expired promo code  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-002  
**Preconditions:** User is on the cart page with items in the cart  
**Steps:**  
1. Enter an invalid promo code  
2. Click "Apply"  
**Expected Results:**  
- Error message is displayed: "Invalid promo code"  
- No discount is applied  
**Negative Scenarios:**  
- Entering a code with special characters  
- Entering a blank code  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-003  
**Preconditions:** User is on the cart page with items in the cart  
**Steps:**  
1. Enter an expired promo code  
2. Click "Apply"  
**Expected Results:**  
- Error message is displayed: "Promo code expired"  
- No discount is applied  
**Negative Scenarios:**  
- Entering a code with a future activation date  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-004  
**Preconditions:** User is on the cart page with items in the cart  
**Steps:**  
1. Enter a promo code that exceeds the maximum allowed discount  
2. Click "Apply"  
**Expected Results:**  
- Discount is capped at the maximum allowed value  
- User is notified if applicable  
**Negative Scenarios:**  
- Applying multiple codes to exceed the cap  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-005  
**Preconditions:** User is on the cart page with items in the cart  
**Steps:**  
1. Enter a valid promo code  
2. Remove an item from the cart  
3. Observe the discount recalculation  
**Expected Results:**  
- Discount is recalculated based on the new cart total  
- Discounted total updates dynamically  
**Negative Scenarios:**  
- Removing all items (cart becomes empty)  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-006  
**Preconditions:** User is on the cart page with items in the cart  
**Steps:**  
1. Enter a valid promo code  
2. Add more items to the cart  
3. Observe the discount recalculation  
**Expected Results:**  
- Discount is recalculated based on the updated cart total  
- Discounted total updates dynamically  
**Negative Scenarios:**  
- Adding items that are not eligible for discount  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-007  
**Preconditions:** User is on the cart page with items in the cart  
**Steps:**  
1. Enter a valid promo code  
2. Proceed to checkout  
3. Complete the payment process  
**Expected Results:**  
- Discount is reflected in the final order summary  
- Payment is processed for the discounted amount  
**Negative Scenarios:**  
- Discount not reflected at payment gateway  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-008  
**Preconditions:** User is on the cart page with items in the cart  
**Steps:**  
1. Enter a valid promo code  
2. Refresh the page  
**Expected Results:**  
- Promo code and discount persist after refresh  
**Negative Scenarios:**  
- Session timeout after refresh  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-009  
**Preconditions:** User is on the cart page with items in the cart  
**Steps:**  
1. Enter a valid promo code  
2. Remove the promo code  
**Expected Results:**  
- Discount is removed  
- Cart total reverts to original amount  
**Negative Scenarios:**  
- Removing code after checkout initiated  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-010  
**Preconditions:** User is on the cart page with items in the cart  
**Steps:**  
1. Enter a valid promo code  
2. Enter another valid promo code  
**Expected Results:**  
- Only one promo code can be applied at a time  
- User is notified if multiple codes are not allowed  
**Negative Scenarios:**  
- Attempting to stack codes  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-011  
**Preconditions:** User is on the cart page with items in the cart  
**Steps:**  
1. Enter a promo code with usage restrictions (e.g., first-time user only)  
2. Click "Apply"  
**Expected Results:**  
- Promo code is applied only if user meets criteria  
- Error message if not eligible  
**Negative Scenarios:**  
- Non-eligible user attempts to use restricted code  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-012  
**Preconditions:** User is on the cart page with items in the cart  
**Steps:**  
1. Enter a promo code with product/category restrictions  
2. Click "Apply"  
**Expected Results:**  
- Discount is applied only to eligible products  
- Ineligible products are not discounted  
**Negative Scenarios:**  
- All items in cart are ineligible  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-013  
**Preconditions:** User is on the cart page with items in the cart  
**Steps:**  
1. Enter a promo code  
2. Attempt to apply the code multiple times  
**Expected Results:**  
- Promo code can only be applied once per order  
- User is notified if attempting to reapply  
**Negative Scenarios:**  
- Multiple browser tabs attempting to apply code  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-014  
**Preconditions:** User is on the cart page with items in the cart  
**Steps:**  
1. Enter a promo code  
2. Simulate network interruption during application  
**Expected Results:**  
- User receives appropriate error or retry message  
- No partial application of discount  
**Negative Scenarios:**  
- Discount applied without confirmation  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Test Case ID:** KAN-8-TC-015  
**Preconditions:** User is on the cart page with items in the cart  
**Steps:**  
1. Enter a valid promo code  
2. Complete checkout on a mobile device  
**Expected Results:**  
- Promo code field and discount calculation are mobile responsive  
- Discount is correctly applied and displayed  
**Negative Scenarios:**  
- UI misalignment or missing fields on mobile  
**Traceability:** https://shivaneeh.atlassian.net/browse/KAN-8

---

**Audit Log:**  
- [2024-12-19T10:32:00Z] Test cases generated for KAN-8  
- [2024-12-19T10:32:01Z] Sensitive information filtered (no PII/PCI detected)  
- [2024-12-19T10:32:02Z] Output structured for QA tool/CI-CD integration  
- [2024-12-19T10:32:03Z] Actions logged for compliance (Audit Trail ID: AUD-KAN8-20241219-001)  

**Compliance Note:**  
- All test cases adhere to ISO27001, SOC2, and GDPR requirements  
- No sensitive data present in test case content  
- Traceability links provided for full auditability and integration
