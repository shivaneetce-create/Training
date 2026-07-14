# Test Case Generation for "Ready" Tickets - Project KAN

## 1. Ticket ID: KAN-55
- **Status:** Ready (In Progress)
- **Summary:** Login throws an error when user attempts related action
- **Traceability:** https://jira.example.com/browse/KAN-55

#### Test Cases:
- **Test Case ID:** TC-KAN-55-01  
  - Preconditions: User is on the login page; valid user credentials exist.
  - Steps: 1. Enter valid username and password. 2. Click 'Login'.
  - Expected Results: User is logged in successfully; no errors are thrown.
  - Negative Scenarios: Invalid credentials, empty fields, locked account.
  - Traceability: KAN-55

- **Test Case ID:** TC-KAN-55-02  
  - Preconditions: User is on login page; invalid credentials available.
  - Steps: 1. Enter invalid username/password. 2. Click 'Login'.
  - Expected Results: Error message displayed; login fails.
  - Negative Scenarios: SQL injection, special characters.
  - Traceability: KAN-55

- **Test Case ID:** TC-KAN-55-03  
  - Preconditions: User is on login page; account is locked.
  - Steps: 1. Enter locked account credentials. 2. Click 'Login'.
  - Expected Results: Locked account error shown.
  - Negative Scenarios: Account lock bypass.
  - Traceability: KAN-55

- **Test Case ID:** TC-KAN-55-04  
  - Preconditions: User is on login page; network is disconnected.
  - Steps: 1. Enter credentials. 2. Click 'Login' with no network.
  - Expected Results: Network error displayed; login fails.
  - Negative Scenarios: Partial connectivity.
  - Traceability: KAN-55

- **Test Case ID:** TC-KAN-55-05  
  - Preconditions: User is on login page; browser cache cleared.
  - Steps: 1. Enter credentials. 2. Click 'Login'.
  - Expected Results: Login works; no errors.
  - Negative Scenarios: Session issues.
  - Traceability: KAN-55

- **Test Case ID:** TC-KAN-55-06  
  - Preconditions: User is on login page; password field empty.
  - Steps: 1. Enter username. 2. Leave password empty. 3. Click 'Login'.
  - Expected Results: Error for empty password.
  - Negative Scenarios: Both fields empty.
  - Traceability: KAN-55

- **Test Case ID:** TC-KAN-55-07  
  - Preconditions: User is on login page; username field empty.
  - Steps: 1. Leave username empty. 2. Enter password. 3. Click 'Login'.
  - Expected Results: Error for empty username.
  - Negative Scenarios: Both fields empty.
  - Traceability: KAN-55

- **Test Case ID:** TC-KAN-55-08  
  - Preconditions: User is on login page; browser is outdated.
  - Steps: 1. Enter credentials. 2. Click 'Login'.
  - Expected Results: Login works or browser compatibility error.
  - Negative Scenarios: Unsupported browser.
  - Traceability: KAN-55

- **Test Case ID:** TC-KAN-55-09  
  - Preconditions: User is on login page; multiple login attempts.
  - Steps: 1. Enter credentials. 2. Click 'Login' repeatedly.
  - Expected Results: Rate limiting or error after threshold.
  - Negative Scenarios: Brute force.
  - Traceability: KAN-55

- **Test Case ID:** TC-KAN-55-10  
  - Preconditions: User is on login page; session expired.
  - Steps: 1. Enter credentials. 2. Click 'Login' after session timeout.
  - Expected Results: Session error or re-login prompt.
  - Negative Scenarios: Session hijack.
  - Traceability: KAN-55

---

## 2. Ticket ID: KAN-50
- **Status:** Ready (In Progress)
- **Summary:** Reporting module does not save changes when user attempts related action
- **Traceability:** https://jira.example.com/browse/KAN-50

#### Test Cases:
- **Test Case ID:** TC-KAN-50-01  
  - Preconditions: User is logged in; reporting module accessible.
  - Steps: 1. Navigate to reporting module. 2. Make changes. 3. Click 'Save'.
  - Expected Results: Changes are saved; confirmation shown.
  - Negative Scenarios: Save fails, no confirmation.
  - Traceability: KAN-50

- **Test Case ID:** TC-KAN-50-02  
  - Preconditions: User is logged in; reporting module accessible.
  - Steps: 1. Make invalid changes. 2. Click 'Save'.
  - Expected Results: Error message for invalid input.
  - Negative Scenarios: Invalid data types.
  - Traceability: KAN-50

- **Test Case ID:** TC-KAN-50-03  
  - Preconditions: User is logged in; reporting module accessible.
  - Steps: 1. Make changes. 2. Disconnect network. 3. Click 'Save'.
  - Expected Results: Network error; changes not saved.
  - Negative Scenarios: Partial save.
  - Traceability: KAN-50

- **Test Case ID:** TC-KAN-50-04  
  - Preconditions: User is logged in; reporting module accessible.
  - Steps: 1. Make changes. 2. Click 'Save' multiple times.
  - Expected Results: Only one save; no duplicate entries.
  - Negative Scenarios: Multiple saves.
  - Traceability: KAN-50

- **Test Case ID:** TC-KAN-50-05  
  - Preconditions: User is logged in; reporting module accessible.
  - Steps: 1. Make changes. 2. Wait for session timeout. 3. Click 'Save'.
  - Expected Results: Session error; changes not saved.
  - Negative Scenarios: Session hijack.
  - Traceability: KAN-50

- **Test Case ID:** TC-KAN-50-06  
  - Preconditions: User is logged in; reporting module accessible.
  - Steps: 1. Make changes. 2. Click 'Save'. 3. Refresh page.
  - Expected Results: Changes persist after refresh.
  - Negative Scenarios: Data loss.
  - Traceability: KAN-50

- **Test Case ID:** TC-KAN-50-07  
  - Preconditions: User is logged in; reporting module accessible.
  - Steps: 1. Make changes. 2. Click 'Save'. 3. Logout and login again.
  - Expected Results: Changes persist after re-login.
  - Negative Scenarios: Data loss.
  - Traceability: KAN-50

- **Test Case ID:** TC-KAN-50-08  
  - Preconditions: User is logged in; reporting module accessible.
  - Steps: 1. Make changes. 2. Click 'Save'. 3. Check audit log.
  - Expected Results: Audit log records change.
  - Negative Scenarios: No audit log.
  - Traceability: KAN-50

- **Test Case ID:** TC-KAN-50-09  
  - Preconditions: User is logged in; reporting module accessible.
  - Steps: 1. Make changes. 2. Click 'Save'. 3. Check for error messages.
  - Expected Results: No errors; changes saved.
  - Negative Scenarios: Error messages shown.
  - Traceability: KAN-50

- **Test Case ID:** TC-KAN-50-10  
  - Preconditions: User is logged in; reporting module accessible.
  - Steps: 1. Make changes. 2. Click 'Save'. 3. Check database for changes.
  - Expected Results: Database reflects changes.
  - Negative Scenarios: Database not updated.
  - Traceability: KAN-50

---

## 3. Ticket ID: KAN-44
- **Status:** Ready (In Progress)
- **Summary:** Onboarding flow crashes on submit when user attempts related action
- **Traceability:** https://jira.example.com/browse/KAN-44

#### Test Cases:
- **Test Case ID:** TC-KAN-44-01  
  - Preconditions: User is on onboarding flow; valid data entered.
  - Steps: 1. Complete onboarding steps. 2. Click 'Submit'.
  - Expected Results: Onboarding completes; no crash.
  - Negative Scenarios: Crash occurs.
  - Traceability: KAN-44

- **Test Case ID:** TC-KAN-44-02  
  - Preconditions: User is on onboarding flow; invalid data entered.
  - Steps: 1. Enter invalid data. 2. Click 'Submit'.
  - Expected Results: Error message; no crash.
  - Negative Scenarios: Crash on invalid data.
  - Traceability: KAN-44

- **Test Case ID:** TC-KAN-44-03  
  - Preconditions: User is on onboarding flow; network disconnected.
  - Steps: 1. Complete onboarding. 2. Click 'Submit' with no network.
  - Expected Results: Network error; no crash.
  - Negative Scenarios: Crash on network error.
  - Traceability: KAN-44

- **Test Case ID:** TC-KAN-44-04  
  - Preconditions: User is on onboarding flow; session expired.
  - Steps: 1. Complete onboarding. 2. Click 'Submit' after session timeout.
  - Expected Results: Session error; no crash.
  - Negative Scenarios: Crash on session timeout.
  - Traceability: KAN-44

- **Test Case ID:** TC-KAN-44-05  
  - Preconditions: User is on onboarding flow; browser is outdated.
  - Steps: 1. Complete onboarding. 2. Click 'Submit'.
  - Expected Results: Onboarding completes; no crash.
  - Negative Scenarios: Crash on unsupported browser.
  - Traceability: KAN-44

- **Test Case ID:** TC-KAN-44-06  
  - Preconditions: User is on onboarding flow; multiple submits.
  - Steps: 1. Complete onboarding. 2. Click 'Submit' multiple times.
  - Expected Results: Only one submission; no crash.
  - Negative Scenarios: Crash on multiple submits.
  - Traceability: KAN-44

- **Test Case ID:** TC-KAN-44-07  
  - Preconditions: User is on onboarding flow; large data input.
  - Steps: 1. Enter large data. 2. Click 'Submit'.
  - Expected Results: Onboarding completes; no crash.
  - Negative Scenarios: Crash on large data.
  - Traceability: KAN-44

- **Test Case ID:** TC-KAN-44-08  
  - Preconditions: User is on onboarding flow; special characters input.
  - Steps: 1. Enter special characters. 2. Click 'Submit'.
  - Expected Results: Onboarding completes; no crash.
  - Negative Scenarios: Crash on special characters.
  - Traceability: KAN-44

- **Test Case ID:** TC-KAN-44-09  
  - Preconditions: User is on onboarding flow; browser cache cleared.
  - Steps: 1. Complete onboarding. 2. Click 'Submit'.
  - Expected Results: Onboarding completes; no crash.
  - Negative Scenarios: Crash on cache issues.
  - Traceability: KAN-44

- **Test Case ID:** TC-KAN-44-10  
  - Preconditions: User is on onboarding flow; audit log enabled.
  - Steps: 1. Complete onboarding. 2. Click 'Submit'. 3. Check audit log.
  - Expected Results: Audit log records submission; no crash.
  - Negative Scenarios: No audit log; crash.
  - Traceability: KAN-44

---

## 4. Ticket ID: KAN-40
- **Status:** Ready (In Progress)
- **Summary:** Dashboard duplicates entries when user attempts related action
- **Traceability:** https://jira.example.com/browse/KAN-40

#### Test Cases:
- **Test Case ID:** TC-KAN-40-01  
  - Preconditions: User is logged in; dashboard accessible.
  - Steps: 1. Navigate to dashboard. 2. Perform action causing duplication.
  - Expected Results: No duplicate entries; dashboard displays unique data.
  - Negative Scenarios: Duplicate entries appear.
  - Traceability: KAN-40

- **Test Case ID:** TC-KAN-40-02  
  - Preconditions: User is logged in; dashboard accessible.
  - Steps: 1. Perform action multiple times. 2. Check for duplicates.
  - Expected Results: No duplicates after repeated actions.
  - Negative Scenarios: Duplicates after multiple actions.
  - Traceability: KAN-40

- **Test Case ID:** TC-KAN-40-03  
  - Preconditions: User is logged in; dashboard accessible.
  - Steps: 1. Perform action with invalid data. 2. Check for duplicates.
  - Expected Results: No duplicates; error message for invalid data.
  - Negative Scenarios: Duplicates with invalid data.
  - Traceability: KAN-40

- **Test Case ID:** TC-KAN-40-04  
  - Preconditions: User is logged in; dashboard accessible.
  - Steps: 1. Perform action with network disconnected. 2. Check for duplicates.
  - Expected Results: No duplicates; network error.
  - Negative Scenarios: Duplicates on network error.
  - Traceability: KAN-40

- **Test Case ID:** TC-KAN-40-05  
  - Preconditions: User is logged in; dashboard accessible.
  - Steps: 1. Perform action. 2. Refresh dashboard.
  - Expected Results: No duplicates after refresh.
  - Negative Scenarios: Duplicates after refresh.
  - Traceability: KAN-40

- **Test Case ID:** TC-KAN-40-06  
  - Preconditions: User is logged in; dashboard accessible.
  - Steps: 1. Perform action. 2. Logout and login again. 3. Check dashboard.
  - Expected Results: No duplicates after re-login.
  - Negative Scenarios: Duplicates after re-login.
  - Traceability: KAN-40

- **Test Case ID:** TC-KAN-40-07  
  - Preconditions: User is logged in; dashboard accessible.
  - Steps: 1. Perform action. 2. Check audit log.
  - Expected Results: Audit log records action; no duplicates.
  - Negative Scenarios: No audit log; duplicates.
  - Traceability: KAN-40

- **Test Case ID:** TC-KAN-40-08  
  - Preconditions: User is logged in; dashboard accessible.
  - Steps: 1. Perform action. 2. Check database for duplicates.
  - Expected Results: Database has unique entries.
  - Negative Scenarios: Database has duplicates.
  - Traceability: KAN-40

- **Test Case ID:** TC-KAN-40-09  
  - Preconditions: User is logged in; dashboard accessible.
  - Steps: 1. Perform action. 2. Check for error messages.
  - Expected Results: No errors; no duplicates.
  - Negative Scenarios: Errors and duplicates.
  - Traceability: KAN-40

- **Test Case ID:** TC-KAN-40-10  
  - Preconditions: User is logged in; dashboard accessible.
  - Steps: 1. Perform action. 2. Check UI for duplicates.
  - Expected Results: UI displays unique entries.
  - Negative Scenarios: UI shows duplicates.
  - Traceability: KAN-40

---

## 5. Ticket ID: KAN-9
- **Status:** Ready (In Progress)
- **Summary:** Implement Promo Code Validation and Dynamic Cart Discount Calculation
- **Traceability:** https://jira.example.com/browse/KAN-9

#### Test Cases:
- **Test Case ID:** TC-KAN-9-01  
  - Preconditions: User is logged in; cart has items; promo code exists.
  - Steps: 1. Navigate to checkout. 2. Enter valid promo code. 3. Apply code.
  - Expected Results: Discount applied; cart total updated.
  - Negative Scenarios: Invalid code, expired code.
  - Traceability: KAN-9

- **Test Case ID:** TC-KAN-9-02  
  - Preconditions: User is logged in; cart has items.
  - Steps: 1. Enter invalid promo code. 2. Apply code.
  - Expected Results: Error message; no discount applied.
  - Negative Scenarios: Malformed code.
  - Traceability: KAN-9

- **Test Case ID:** TC-KAN-9-03  
  - Preconditions: User is logged in; cart has items.
  - Steps: 1. Enter expired promo code. 2. Apply code.
  - Expected Results: Error message; no discount applied.
  - Negative Scenarios: Expired code.
  - Traceability: KAN-9

- **Test Case ID:** TC-KAN-9-04  
  - Preconditions: User is logged in; cart has items.
  - Steps: 1. Enter promo code. 2. Remove code. 3. Reapply code.
  - Expected Results: Discount applied and removed correctly.
  - Negative Scenarios: Discount not removed.
  - Traceability: KAN-9

- **Test Case ID:** TC-KAN-9-05  
  - Preconditions: User is logged in; cart has items.
  - Steps: 1. Enter promo code. 2. Apply code. 3. Checkout.
  - Expected Results: Discount persists through checkout.
  - Negative Scenarios: Discount lost at checkout.
  - Traceability: KAN-9

- **Test Case ID:** TC-KAN-9-06  
  - Preconditions: User is logged in; cart has items.
  - Steps: 1. Enter promo code. 2. Apply code. 3. Refresh page.
  - Expected Results: Discount persists after refresh.
  - Negative Scenarios: Discount lost after refresh.
  - Traceability: KAN-9

- **Test Case ID:** TC-KAN-9-07  
  - Preconditions: User is logged in; cart has items.
  - Steps: 1. Enter promo code. 2. Apply code. 3. Logout and login again.
  - Expected Results: Discount persists after re-login.
  - Negative Scenarios: Discount lost after re-login.
  - Traceability: KAN-9

- **Test Case ID:** TC-KAN-9-08  
  - Preconditions: User is logged in; cart has items.
  - Steps: 1. Enter promo code. 2. Apply code. 3. Check audit log.
  - Expected Results: Audit log records promo code application.
  - Negative Scenarios: No audit log.
  - Traceability: KAN-9

- **Test Case ID:** TC-KAN-9-09  
  - Preconditions: User is logged in; cart has items.
  - Steps: 1. Enter promo code. 2. Apply code. 3. Check database for discount.
  - Expected Results: Database reflects discount.
  - Negative Scenarios: Database not updated.
  - Traceability: KAN-9

- **Test Case ID:** TC-KAN-9-10  
  - Preconditions: User is logged in; cart has items.
  - Steps: 1. Enter promo code. 2. Apply code. 3. Check UI for discount.
  - Expected Results: UI displays updated cart total.
  - Negative Scenarios: UI not updated.
  - Traceability: KAN-9

---

## 6. Ticket ID: KAN-1
- **Status:** Ready (In Progress)
- **Summary:** Task 1
- **Traceability:** https://jira.example.com/browse/KAN-1

#### Test Cases:
- **Test Case ID:** TC-KAN-1-01  
  - Preconditions: Task 1 requirements defined.
  - Steps: 1. Review requirements. 2. Execute Task 1 as per instructions.
  - Expected Results: Task 1 completed successfully.
  - Negative Scenarios: Missing requirements, incomplete execution.
  - Traceability: KAN-1

- **Test Case ID:** TC-KAN-1-02  
  - Preconditions: Task 1 requirements defined.
  - Steps: 1. Execute Task 1 with invalid input.
  - Expected Results: Error message; task not completed.
  - Negative Scenarios: Invalid input.
  - Traceability: KAN-1

- **Test Case ID:** TC-KAN-1-03  
  - Preconditions: Task 1 requirements defined.
  - Steps: 1. Execute Task 1 with network disconnected.
  - Expected Results: Network error; task not completed.
  - Negative Scenarios: Partial completion.
  - Traceability: KAN-1

- **Test Case ID:** TC-KAN-1-04  
  - Preconditions: Task 1 requirements defined.
  - Steps: 1. Execute Task 1 multiple times.
  - Expected Results: No duplicate results.
  - Negative Scenarios: Duplicate results.
  - Traceability: KAN-1

- **Test Case ID:** TC-KAN-1-05  
  - Preconditions: Task 1 requirements defined.
  - Steps: 1. Execute Task 1. 2. Refresh page.
  - Expected Results: Task persists after refresh.
  - Negative Scenarios: Task lost after refresh.
  - Traceability: KAN-1

- **Test Case ID:** TC-KAN-1-06  
  - Preconditions: Task 1 requirements defined.
  - Steps: 1. Execute Task 1. 2. Logout and login again.
  - Expected Results: Task persists after re-login.
  - Negative Scenarios: Task lost after re-login.
  - Traceability: KAN-1

- **Test Case ID:** TC-KAN-1-07  
  - Preconditions: Task 1 requirements defined.
  - Steps: 1. Execute Task 1. 2. Check audit log.
  - Expected Results: Audit log records task execution.
  - Negative Scenarios: No audit log.
  - Traceability: KAN-1

- **Test Case ID:** TC-KAN-1-08  
  - Preconditions: Task 1 requirements defined.
  - Steps: 1. Execute Task 1. 2. Check database for results.
  - Expected Results: Database reflects task completion.
  - Negative Scenarios: Database not updated.
  - Traceability: KAN-1

- **Test Case ID:** TC-KAN-1-09  
  - Preconditions: Task 1 requirements defined.
  - Steps: 1. Execute Task 1. 2. Check UI for results.
  - Expected Results: UI displays task completion.
  - Negative Scenarios: UI not updated.
  - Traceability: KAN-1

- **Test Case ID:** TC-KAN-1-10  
  - Preconditions: Task 1 requirements defined.
  - Steps: 1. Execute Task 1. 2. Check for error messages.
  - Expected Results: No errors; task completed.
  - Negative Scenarios: Errors shown.
  - Traceability: KAN-1

---

## Tickets Not Ready

For all other tickets, output:
> The Story is currently not ready and hence the test cases could not be generated.

---

**Compliance Note:** All actions and outputs have been logged for auditing. No sensitive information included.  
**Output is structured for integration with QA tools and CI/CD pipelines.**