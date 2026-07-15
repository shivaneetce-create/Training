# Test Cases for Reporting Module Save Changes Issue (KAN-50)

## JIRA Ticket Details
- **Ticket ID:** KAN-50
- **Status:** Ready (In Progress)
- **Summary:** Reporting module does not save changes when user attempts related action
- **Description:** The reporting module is experiencing an issue where changes are not being saved when users perform standard actions.
- **Environment:** Production environment, affects multiple users.
- **Priority:** Medium
- **Issue Type:** Task
- **Last Updated:** July 14, 2026
- **Traceability:** https://jira.example.com/browse/KAN-50

---

## Test Cases

### TC-KAN-50-001
- **Preconditions:** User is logged in with valid credentials; reporting module is accessible; no unsaved changes exist.
- **Steps:**
  1. Navigate to the reporting module section.
  2. Perform a standard user action that modifies report data (e.g., edit a report field).
  3. Click 'Save' or equivalent action.
- **Expected Results:** Changes are saved successfully; confirmation message is displayed.
- **Negative Scenarios:** Attempt to save with invalid data; network interruption during save.

---

### TC-KAN-50-002
- **Preconditions:** User is logged in; reporting module contains existing reports.
- **Steps:**
  1. Open an existing report.
  2. Make multiple changes to report fields.
  3. Click 'Save'.
  4. Refresh the page.
- **Expected Results:** All changes persist after refresh; no data loss.
- **Negative Scenarios:** Attempt to save with empty required fields; session timeout before save.

---

### TC-KAN-50-003
- **Preconditions:** User is logged in; reporting module is accessible; user has edit permissions.
- **Steps:**
  1. Attempt to save changes without making any modifications.
- **Expected Results:** System displays 'No changes to save' or similar message; no errors.
- **Negative Scenarios:** System attempts to save and throws an error.

---

### TC-KAN-50-004
- **Preconditions:** User is logged in; reporting module is accessible; user has edit permissions.
- **Steps:**
  1. Make changes to a report.
  2. Attempt to navigate away without saving.
  3. Observe warning or prompt.
- **Expected Results:** User is warned about unsaved changes; option to save or discard.
- **Negative Scenarios:** No warning is shown; changes are lost without notice.

---

### TC-KAN-50-005
- **Preconditions:** User is logged in; reporting module is accessible; user has edit permissions.
- **Steps:**
  1. Make changes to a report.
  2. Save changes.
  3. Log out and log back in.
  4. Reopen the report.
- **Expected Results:** Changes persist after logout/login; data integrity maintained.
- **Negative Scenarios:** Changes are lost after logout; report reverts to previous state.

---

### TC-KAN-50-006
- **Preconditions:** User is logged in; reporting module is accessible; user has edit permissions.
- **Steps:**
  1. Make changes to a report.
  2. Save changes.
  3. Attempt to save again immediately.
- **Expected Results:** System prevents duplicate saves; displays appropriate message.
- **Negative Scenarios:** System allows duplicate saves; creates redundant entries.

---

### TC-KAN-50-007
- **Preconditions:** User is logged in; reporting module is accessible; user has edit permissions.
- **Steps:**
  1. Make changes to a report.
  2. Disconnect network before saving.
  3. Attempt to save changes.
- **Expected Results:** System displays error message; changes are not saved.
- **Negative Scenarios:** System hangs or crashes; no error message shown.

---

### TC-KAN-50-008
- **Preconditions:** User is logged in; reporting module is accessible; user has edit permissions.
- **Steps:**
  1. Make changes to a report.
  2. Save changes.
  3. Check audit log for save action.
- **Expected Results:** Audit log records the save action with timestamp and user ID.
- **Negative Scenarios:** No audit log entry; incorrect log details.

---

### TC-KAN-50-009
- **Preconditions:** User is logged in; reporting module is accessible; user has edit permissions.
- **Steps:**
  1. Attempt to save changes with invalid input (e.g., special characters, SQL injection).
- **Expected Results:** System validates input; displays error message; changes are not saved.
- **Negative Scenarios:** System accepts invalid input; data corruption occurs.

---

### TC-KAN-50-010
- **Preconditions:** User is logged in; reporting module is accessible; user has edit permissions.
- **Steps:**
  1. Make changes to a report.
  2. Save changes.
  3. Attempt to access the report from another user account.
- **Expected Results:** Changes are visible to other users if permissions allow; data consistency maintained.
- **Negative Scenarios:** Changes are not visible; data inconsistency between users.

---

*All actions have been logged for audit purposes. Sensitive information has been filtered from the output. Test cases are structured for integration with QA tools and CI/CD pipelines.*