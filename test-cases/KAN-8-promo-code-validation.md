# Test Cases for KAN-8: Implement Promo Code Validation and Dynamic Cart Discount Calculation

---

**Test Case ID:** KAN-8-TC-001  
**Preconditions:** User is logged in and has items in the cart  
**Steps:**  
1. Navigate to the cart page  
2. Enter a valid promo code in the promo code field  
3. Click "Apply"  
**Expected Results:**  
- Promo code is accepted  
- Discount is applied to the cart total dynamically  
- Success message is displayed  
**Negative Scenarios:**  
- Promo code expired  
- Promo code usage limit reached  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** KAN-8-TC-002  
**Preconditions:** User is on the cart page with items  
**Steps:**  
1. Enter an invalid promo code (e.g., random string)  
2. Click "Apply"  
**Expected Results:**  
- Error message: "Invalid promo code"  
- No discount applied  
**Negative Scenarios:**  
- SQL injection attempt in promo code field  
- XSS payload in promo code field  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** KAN-8-TC-003  
**Preconditions:** User is on the cart page  
**Steps:**  
1. Enter a promo code that has expired  
2. Click "Apply"  
**Expected Results:**  
- Error message: "Promo code expired"  
- No discount applied  
**Negative Scenarios:**  
- System clock manipulation  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** KAN-8-TC-004  
**Preconditions:** User is on the cart page  
**Steps:**  
1. Enter a promo code that is not applicable to the items in the cart  
2. Click "Apply"  
**Expected Results:**  
- Error message: "Promo code not applicable to selected items"  
- No discount applied  
**Negative Scenarios:**  
- Cart contains mixed eligible and ineligible items  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** KAN-8-TC-005  
**Preconditions:** User is on the cart page  
**Steps:**  
1. Enter a valid promo code  
2. Remove an item from the cart  
**Expected Results:**  
- Discount recalculates dynamically  
- If cart no longer meets promo code criteria, discount is removed and user is notified  
**Negative Scenarios:**  
- Rapid add/remove actions  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** KAN-8-TC-006  
**Preconditions:** User is on the cart page  
**Steps:**  
1. Enter a valid promo code  
2. Proceed to checkout  
3. Complete payment  
**Expected Results:**  
- Discount is reflected in the final payment amount  
- Promo code usage is logged  
**Negative Scenarios:**  
- Network failure during checkout  
- Payment gateway error  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** KAN-8-TC-007  
**Preconditions:** User is on the cart page  
**Steps:**  
1. Enter a promo code with a usage limit (e.g., first 100 users)  
2. If limit reached, attempt to apply  
**Expected Results:**  
- Error message: "Promo code usage limit reached"  
- No discount applied  
**Negative Scenarios:**  
- Simultaneous usage by multiple users  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** KAN-8-TC-008  
**Preconditions:** User is on the cart page  
**Steps:**  
1. Enter a valid promo code  
2. Refresh the page  
**Expected Results:**  
- Discount remains applied after refresh  
- Promo code field retains value  
**Negative Scenarios:**  
- Session timeout  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** KAN-8-TC-009  
**Preconditions:** User is on the cart page  
**Steps:**  
1. Enter a valid promo code  
2. Log out and log back in  
3. Return to cart  
**Expected Results:**  
- Discount is still applied if cart is persistent  
- Promo code is not lost  
**Negative Scenarios:**  
- Cart data loss  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** KAN-8-TC-010  
**Preconditions:** User is on the cart page  
**Steps:**  
1. Enter a valid promo code  
2. Attempt to apply the same promo code again  
**Expected Results:**  
- Message: "Promo code already applied"  
- No duplicate discounts  
**Negative Scenarios:**  
- Multiple browser tabs  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** KAN-8-TC-011  
**Preconditions:** User is on the cart page  
**Steps:**  
1. Enter a valid promo code  
2. Remove the promo code  
**Expected Results:**  
- Discount is removed  
- Cart total updates accordingly  
**Negative Scenarios:**  
- Undo/redo actions  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** KAN-8-TC-012  
**Preconditions:** User is on the cart page  
**Steps:**  
1. Enter a promo code with minimum cart value requirement  
2. Ensure cart value is below minimum  
3. Click "Apply"  
**Expected Results:**  
- Error message: "Cart value does not meet minimum requirement"  
- No discount applied  
**Negative Scenarios:**  
- Cart value changes after applying code  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** KAN-8-TC-013  
**Preconditions:** User is on the cart page  
**Steps:**  
1. Enter a valid promo code  
2. Attempt to apply a second promo code  
**Expected Results:**  
- Message: "Only one promo code can be applied at a time"  
- Only first code is active  
**Negative Scenarios:**  
- Attempt to stack codes via API  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Test Case ID:** KAN-8-TC-014  
**Preconditions:** User is on the cart page  
**Steps:**  
1. Enter a valid promo code  
2. Simulate rapid repeated submissions (rate limiting test)  
**Expected Results:**  
- System enforces rate limiting  
- Error message: "Too many attempts, please try again later"  
**Negative Scenarios:**  
- Automated script attempts  
**Traceability:** [KAN-8](https://shivaneeh.atlassian.net/browse/KAN-8)

---

**Audit Log:**  
- [2024-12-19T10:30:00Z] Issue KAN-8 test cases generated  
- All test cases filtered for sensitive information  
- Actions logged for compliance and traceability  
- Output structured for QA tool and CI/CD pipeline integration

**End of Output**