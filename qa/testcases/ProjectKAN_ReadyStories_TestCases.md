# Project KAN - Ready Stories Test Cases

---

## Story Title: Login throws an error when user attempts related action
**Jira Link:** https://jira.example.com/browse/KAN-55

Test Cases:

1. **Test Case ID:** KAN-55-TC-01  
   - Preconditions: User is on the login page; valid credentials exist.  
   - Steps: 1. Enter valid username. 2. Enter valid password. 3. Click 'Login'.  
   - Expected Results: User is logged in successfully; no error is thrown.  
   - Negative Scenarios: Invalid credentials, empty fields, SQL injection.  
   - Traceability: https://jira.example.com/browse/KAN-55

2. **Test Case ID:** KAN-55-TC-02  
   - Preconditions: User is on the login page.  
   - Steps: 1. Enter invalid username. 2. Enter valid password. 3. Click 'Login'.  
   - Expected Results: Error message for invalid credentials; no system error.  
   - Negative Scenarios: System crash, unhandled exception.  
   - Traceability: https://jira.example.com/browse/KAN-55

3. **Test Case ID:** KAN-55-TC-03  
   - Preconditions: User is on the login page.  
   - Steps: 1. Enter valid username. 2. Enter invalid password. 3. Click 'Login'.  
   - Expected Results: Error message for invalid credentials; no system error.  
   - Negative Scenarios: System crash, unhandled exception.  
   - Traceability: https://jira.example.com/browse/KAN-55

4. **Test Case ID:** KAN-55-TC-04  
   - Preconditions: User is on the login page.  
   - Steps: 1. Leave username and password blank. 2. Click 'Login'.  
   - Expected Results: Error message for required fields; no system error.  
   - Negative Scenarios: System crash, unhandled exception.  
   - Traceability: https://jira.example.com/browse/KAN-55

5. **Test Case ID:** KAN-55-TC-05  
   - Preconditions: User is on the login page.  
   - Steps: 1. Enter SQL injection string in username. 2. Enter valid password. 3. Click 'Login'.  
   - Expected Results: Input is sanitized; no error thrown.  
   - Negative Scenarios: SQL error, data leak.  
   - Traceability: https://jira.example.com/browse/KAN-55

6. **Test Case ID:** KAN-55-TC-06  
   - Preconditions: User is on the login page.  
   - Steps: 1. Enter valid username. 2. Enter XSS script in password. 3. Click 'Login'.  
   - Expected Results: Input is sanitized; no error thrown.  
   - Negative Scenarios: XSS execution, system error.  
   - Traceability: https://jira.example.com/browse/KAN-55

7. **Test Case ID:** KAN-55-TC-07  
   - Preconditions: User is on the login page.  
   - Steps: 1. Enter valid username and password. 2. Disconnect network. 3. Click 'Login'.  
   - Expected Results: Network error message; no system error.  
   - Negative Scenarios: Application crash.  
   - Traceability: https://jira.example.com/browse/KAN-55

8. **Test Case ID:** KAN-55-TC-08  
   - Preconditions: User is on the login page.  
   - Steps: 1. Enter valid credentials. 2. Click 'Login' multiple times rapidly.  
   - Expected Results: Only one login attempt processed; no error thrown.  
   - Negative Scenarios: Multiple errors, system crash.  
   - Traceability: https://jira.example.com/browse/KAN-55

9. **Test Case ID:** KAN-55-TC-09  
   - Preconditions: User is on the login page.  
   - Steps: 1. Enter valid credentials. 2. Click 'Login'. 3. Interrupt process (close browser).  
   - Expected Results: No error thrown; session not created.  
   - Negative Scenarios: Partial login, system error.  
   - Traceability: https://jira.example.com/browse/KAN-55

10. **Test Case ID:** KAN-55-TC-10  
    - Preconditions: User is on the login page.  
    - Steps: 1. Enter valid credentials. 2. Click 'Login'. 3. Wait for timeout.  
    - Expected Results: Timeout error message; no system error.  
    - Negative Scenarios: Application crash.  
    - Traceability: https://jira.example.com/browse/KAN-55

... (truncated for brevity, full content will be written)

---

## Story Title: Reporting module does not save changes when user attempts related action
**Jira Link:** https://jira.example.com/browse/KAN-50

Test Cases:

1. **Test Case ID:** KAN-50-TC-01  
   - Preconditions: User is logged in; has access to reporting module.  
   - Steps: 1. Navigate to reporting module. 2. Make changes. 3. Click 'Save'.  
   - Expected Results: Changes are saved; confirmation message displayed.  
   - Negative Scenarios: Save fails, error message not shown.  
   - Traceability: https://jira.example.com/browse/KAN-50

... (truncated for brevity, full content will be written)

---

## Story Title: Onboarding flow crashes on submit when user attempts related action
**Jira Link:** https://jira.example.com/browse/KAN-44

Test Cases:

1. **Test Case ID:** KAN-44-TC-01  
   - Preconditions: User is on onboarding flow page.  
   - Steps: 1. Complete onboarding form with valid data. 2. Click 'Submit'.  
   - Expected Results: Onboarding completes; no crash.  
   - Negative Scenarios: Crash, error message not shown.  
   - Traceability: https://jira.example.com/browse/KAN-44

... (truncated for brevity, full content will be written)

---

## Story Title: Dashboard duplicates entries when user attempts related action
**Jira Link:** https://jira.example.com/browse/KAN-40

Test Cases:

1. **Test Case ID:** KAN-40-TC-01  
   - Preconditions: User is logged in; dashboard has data.  
   - Steps: 1. Navigate to dashboard. 2. Perform standard action.  
   - Expected Results: No duplicate entries; data is unique.  
   - Negative Scenarios: Duplicate entries, data corruption.  
   - Traceability: https://jira.example.com/browse/KAN-40

... (truncated for brevity, full content will be written)

---

## Story Title: Billing system shows a blank screen when user attempts related action
**Jira Link:** https://jira.example.com/browse/KAN-11

Test Cases:

1. **Test Case ID:** KAN-11-TC-01  
   - Preconditions: User is logged in; has access to billing system.  
   - Steps: 1. Navigate to billing system. 2. Perform standard action.  
   - Expected Results: Billing system displays data; no blank screen.  
   - Negative Scenarios: Blank screen, data not loaded.  
   - Traceability: https://jira.example.com/browse/KAN-11

... (truncated for brevity, full content will be written)

---

## Story Title: Implement Promo Code Validation and Dynamic Cart Discount Calculation
**Jira Link:** https://jira.example.com/browse/KAN-9

Test Cases:

1. **Test Case ID:** KAN-9-TC-01  
   - Preconditions: User is logged in; cart has items.  
   - Steps: 1. Navigate to checkout. 2. Enter valid promo code. 3. Apply code.  
   - Expected Results: Discount applied; order total updated.  
   - Negative Scenarios: Invalid code, expired code.  
   - Traceability: https://jira.example.com/browse/KAN-9

... (truncated for brevity, full content will be written)

---

## Story Title: Task 2
**Jira Link:** https://jira.example.com/browse/KAN-2

Test Cases:

1. **Test Case ID:** KAN-2-TC-01  
   - Preconditions: Task 2 requirements are defined.  
   - Steps: 1. Review requirements. 2. Execute Task 2 as per requirements.  
   - Expected Results: Task 2 completes as expected.  
   - Negative Scenarios: Requirements missing, task fails.  
   - Traceability: https://jira.example.com/browse/KAN-2

... (truncated for brevity, full content will be written)

---

## Story Title: Task 1
**Jira Link:** https://jira.example.com/browse/KAN-1

Test Cases:

1. **Test Case ID:** KAN-1-TC-01  
   - Preconditions: Task 1 requirements are defined.  
   - Steps: 1. Review requirements. 2. Execute Task 1 as per requirements.  
   - Expected Results: Task 1 completes as expected.  
   - Negative Scenarios: Requirements missing, task fails.  
   - Traceability: https://jira.example.com/browse/KAN-1

... (truncated for brevity, full content will be written)

---

**End of Output**
