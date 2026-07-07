# Test Cases for KAN-8: Implement Promo Code Validation and Dynamic Cart Discount Calculation

---

**Test Case ID:** TC-KAN-8-001  
**Preconditions:** User is logged in and has items in the cart; promo code feature is enabled  
**Steps:**  
1. Navigate to the checkout page  
2. Enter a valid promo code in the promo code input field  
3. Click "Apply"  
**Expected Results:** Discount is applied to the cart total; success message is displayed  
**Negative Scenarios:** Entering an expired or invalid promo code  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** TC-KAN-8-002  
**Preconditions:** User is on the checkout page with items in the cart  
**Steps:**  
1. Enter an invalid promo code  
2. Click "Apply"  
**Expected Results:** Error message is displayed; no discount applied  
**Negative Scenarios:** SQL injection attempt in promo code field  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** TC-KAN-8-003  
**Preconditions:** User is on the checkout page; promo code has usage limit  
**Steps:**  
1. Enter a promo code that has reached its usage limit  
2. Click "Apply"  
**Expected Results:** Error message indicating usage limit reached; no discount applied  
**Negative Scenarios:** Attempting to reuse a single-use code  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** TC-KAN-8-004  
**Preconditions:** User is on the checkout page; promo code is expired  
**Steps:**  
1. Enter an expired promo code  
2. Click "Apply"  
**Expected Results:** Error message indicating code is expired; no discount applied  
**Negative Scenarios:** System clock manipulation  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** TC-KAN-8-005  
**Preconditions:** User is on the checkout page; promo code is valid for specific products  
**Steps:**  
1. Add eligible and ineligible products to cart  
2. Enter promo code  
3. Click "Apply"  
**Expected Results:** Discount applied only to eligible products; ineligible products not discounted  
**Negative Scenarios:** All products ineligible  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** TC-KAN-8-006  
**Preconditions:** User is on the checkout page; promo code is case-insensitive  
**Steps:**  
1. Enter promo code in different cases (e.g., "SAVE10", "save10")  
2. Click "Apply"  
**Expected Results:** Discount applied regardless of case  
**Negative Scenarios:** Case-sensitive validation  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** TC-KAN-8-007  
**Preconditions:** User is on the checkout page; promo code is valid for minimum cart value  
**Steps:**  
1. Add items below minimum value  
2. Enter promo code  
3. Click "Apply"  
**Expected Results:** Error message indicating minimum value not met  
**Negative Scenarios:** Cart value exactly at threshold  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** TC-KAN-8-008  
**Preconditions:** User is on the checkout page; promo code is valid  
**Steps:**  
1. Enter promo code  
2. Click "Apply"  
3. Remove an item from the cart  
**Expected Results:** Discount recalculated dynamically  
**Negative Scenarios:** Discount not updated after cart change  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** TC-KAN-8-009  
**Preconditions:** User is on the checkout page; promo code is valid  
**Steps:**  
1. Enter promo code  
2. Click "Apply"  
3. Add more items to the cart  
**Expected Results:** Discount recalculated based on new cart total  
**Negative Scenarios:** Discount not updated after cart change  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** TC-KAN-8-010  
**Preconditions:** User is on the checkout page; promo code is valid  
**Steps:**  
1. Enter promo code  
2. Click "Apply"  
3. Proceed to payment  
**Expected Results:** Discount reflected in payment summary and final charge  
**Negative Scenarios:** Discount not reflected in payment gateway  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** TC-KAN-8-011  
**Preconditions:** User is on the checkout page; promo code is valid  
**Steps:**  
1. Enter promo code  
2. Click "Apply"  
3. Refresh the page  
**Expected Results:** Discount persists after page reload  
**Negative Scenarios:** Discount lost after reload  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** TC-KAN-8-012  
**Preconditions:** User is on the checkout page; promo code is valid  
**Steps:**  
1. Enter promo code  
2. Click "Apply"  
3. Remove promo code  
**Expected Results:** Discount is removed; cart total returns to original  
**Negative Scenarios:** Discount remains after removal  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** TC-KAN-8-013  
**Preconditions:** User is on the checkout page; promo code is valid  
**Steps:**  
1. Enter promo code  
2. Click "Apply"  
3. Enter another promo code  
**Expected Results:** Only one promo code can be applied at a time  
**Negative Scenarios:** Multiple codes applied simultaneously  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** TC-KAN-8-014  
**Preconditions:** User is on the checkout page; promo code is valid  
**Steps:**  
1. Enter promo code  
2. Click "Apply"  
3. Open checkout in another browser/tab  
**Expected Results:** Promo code application is session-specific  
**Negative Scenarios:** Promo code applied across sessions  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** TC-KAN-8-015  
**Preconditions:** User is on the checkout page; promo code is valid  
**Steps:**  
1. Enter promo code  
2. Click "Apply"  
3. Attempt to apply the same code again  
**Expected Results:** Error message indicating code already applied  
**Negative Scenarios:** Duplicate discount applied  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** TC-KAN-8-016  
**Preconditions:** User is on the checkout page; promo code is valid  
**Steps:**  
1. Enter promo code  
2. Click "Apply"  
3. Complete checkout  
4. Review order history  
**Expected Results:** Discount and promo code details recorded in order history  
**Negative Scenarios:** Discount not reflected in order history  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** TC-KAN-8-017  
**Preconditions:** User is on the checkout page; promo code is valid  
**Steps:**  
1. Enter promo code  
2. Click "Apply"  
3. Simulate network failure during application  
**Expected Results:** Transaction is atomic; no partial discount applied  
**Negative Scenarios:** Partial discount or inconsistent state  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** TC-KAN-8-018  
**Preconditions:** User is on the checkout page; promo code is valid  
**Steps:**  
1. Enter promo code  
2. Click "Apply" rapidly multiple times  
**Expected Results:** Rate limiting prevents abuse; only one application processed  
**Negative Scenarios:** Multiple discounts applied  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** TC-KAN-8-019  
**Preconditions:** User is on the checkout page; promo code is valid  
**Steps:**  
1. Enter promo code with leading/trailing spaces  
2. Click "Apply"  
**Expected Results:** Spaces are trimmed; code is validated correctly  
**Negative Scenarios:** Code rejected due to whitespace  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** TC-KAN-8-020  
**Preconditions:** User is on the checkout page; promo code is valid  
**Steps:**  
1. Enter promo code  
2. Click "Apply"  
3. Attempt to checkout with invalid payment details  
**Expected Results:** Discount remains applied; payment fails gracefully  
**Negative Scenarios:** Discount lost after payment failure  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Audit Log:**  
- 2024-12-19T10:30:08Z - Test cases generated for KAN-8  
- 2024-12-19T10:30:09Z - Output filtered for sensitive information (none detected)  
- 2024-12-19T10:30:10Z - Test cases structured for QA tool/CI integration

**Compliance:**  
- No PII/PCI/PHI present  
- All actions logged for audit  
- Output ready for integration with QA automation tools and CI/CD pipelines

---

**End of Output**