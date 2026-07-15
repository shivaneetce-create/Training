---
Ticket ID: KAN-9
Status: Ready (In Progress)
Assignee: Unassigned
Summary: Implement Promo Code Validation and Dynamic Cart Discount Calculation
Description: No description provided for this ticket.
Attachments: No attachments available.
Created On: July 8, 2026
Updated On: July 10, 2026
Comments: No comments available for this ticket.
Priority: Medium
Issue Type: Story
Sprint: Not assigned to any sprint
Story Points: Not estimated
---

Plain Language Summary:
Ticket KAN-9 is currently unassigned and has a status of "Ready" (categorized as In Progress). The ticket is a Story titled "Implement Promo Code Validation and Dynamic Cart Discount Calculation" and was created on July 8, 2026. It has a medium priority level. There is no detailed description, no comments from team members, and no attachments associated with this ticket. The story has not been assigned story points and is not part of any sprint yet.
---
Compliance Note: All information presented has been filtered for sensitive data (PII/PHI/PCI). Only publicly accessible project information is displayed. Access and retrieval actions have been logged for audit purposes in accordance with enterprise security standards.
----------
Story Title: Implement Promo Code Validation and Dynamic Cart Discount Calculation
Test Cases:
---
Test Case ID: KAN-9-TC-001  
Preconditions: User is logged in; cart contains at least one item; promo code field is visible.  
Steps:  
1. Enter a valid promo code.  
2. Click "Apply".  
Expected Results: Promo code is validated; discount is applied to cart total; success message is displayed.  
Negative Scenarios: Entering an expired or invalid promo code.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-002  
Preconditions: User is logged in; cart contains multiple items; promo code field is visible.  
Steps:  
1. Enter a valid promo code.  
2. Click "Apply".  
Expected Results: Discount is distributed correctly across all items; cart total reflects discount.  
Negative Scenarios: Applying promo code with ineligible items in cart.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-003  
Preconditions: User is logged in; cart is empty.  
Steps:  
1. Enter a valid promo code.  
2. Click "Apply".  
Expected Results: Error message indicating cart must have items to apply promo code.  
Negative Scenarios: Attempting to apply promo code with no items.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-004  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Enter an invalid promo code.  
2. Click "Apply".  
Expected Results: Error message indicating invalid promo code; no discount applied.  
Negative Scenarios: Typo in promo code.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-005  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Enter an expired promo code.  
2. Click "Apply".  
Expected Results: Error message indicating promo code is expired; no discount applied.  
Negative Scenarios: Using a promo code past its validity date.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-006  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Enter a promo code not applicable to any cart items.  
2. Click "Apply".  
Expected Results: Error message indicating promo code not applicable; no discount applied.  
Negative Scenarios: Promo code for electronics used on clothing.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-007  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Enter a promo code with usage limit reached.  
2. Click "Apply".  
Expected Results: Error message indicating promo code usage limit reached; no discount applied.  
Negative Scenarios: Promo code used maximum allowed times.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-008  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Enter a promo code with minimum cart value requirement not met.  
2. Click "Apply".  
Expected Results: Error message indicating minimum cart value not met; no discount applied.  
Negative Scenarios: Cart value below promo code threshold.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-009  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Enter a promo code with maximum discount cap.  
2. Click "Apply".  
Expected Results: Discount applied up to maximum cap; cart total reflects capped discount.  
Negative Scenarios: Cart value high enough to exceed discount cap.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-010  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Enter a promo code with percentage discount.  
2. Click "Apply".  
Expected Results: Percentage discount correctly calculated and applied to cart total.  
Negative Scenarios: Incorrect percentage calculation.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-011  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Enter a promo code with fixed amount discount.  
2. Click "Apply".  
Expected Results: Fixed amount discount correctly subtracted from cart total.  
Negative Scenarios: Discount exceeds cart total.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-012  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Enter a promo code with both percentage and fixed amount options.  
2. Click "Apply".  
Expected Results: Correct discount type applied as per promo code configuration.  
Negative Scenarios: Both discounts applied simultaneously.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-013  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Enter a promo code with product-specific applicability.  
2. Click "Apply".  
Expected Results: Discount applied only to eligible products in cart.  
Negative Scenarios: Discount applied to ineligible products.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-014  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Enter a promo code with category-specific applicability.  
2. Click "Apply".  
Expected Results: Discount applied only to eligible categories in cart.  
Negative Scenarios: Discount applied to non-eligible categories.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-015  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Enter a promo code with user-specific restriction.  
2. Click "Apply".  
Expected Results: Discount applied only if user is eligible.  
Negative Scenarios: Ineligible user attempts to apply code.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-016  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Enter a promo code with first-time user restriction.  
2. Click "Apply".  
Expected Results: Discount applied only for first-time users.  
Negative Scenarios: Returning user attempts to apply code.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-017  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Enter a promo code with one-time use per user restriction.  
2. Click "Apply".  
Expected Results: Discount applied only if user has not used code before.  
Negative Scenarios: User tries to reuse code.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-018  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Enter a promo code with start and end date.  
2. Click "Apply" within validity period.  
Expected Results: Discount applied successfully.  
Negative Scenarios: Applying code before start or after end date.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-019  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Enter a promo code with case sensitivity.  
2. Enter code in different case.  
3. Click "Apply".  
Expected Results: Promo code validation is case-insensitive (if applicable).  
Negative Scenarios: Case-sensitive codes rejected.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-020  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Enter a promo code with whitespace before/after.  
2. Click "Apply".  
Expected Results: Whitespace is trimmed; code is validated correctly.  
Negative Scenarios: Whitespace causes code rejection.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-021  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Enter a promo code with special characters.  
2. Click "Apply".  
Expected Results: Promo code is validated correctly.  
Negative Scenarios: Special characters cause validation failure.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-022  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Enter a promo code and click "Apply" multiple times rapidly.  
Expected Results: Discount applied only once; no duplicate application.  
Negative Scenarios: Multiple discounts applied.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-023  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Apply a valid promo code.  
2. Remove an item from cart.  
Expected Results: Discount recalculated dynamically; cart total updated.  
Negative Scenarios: Discount not updated after cart change.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-024  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Apply a valid promo code.  
2. Add more items to cart.  
Expected Results: Discount recalculated dynamically; cart total updated.  
Negative Scenarios: Discount not updated after cart change.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-025  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Apply a valid promo code.  
2. Change quantity of items in cart.  
Expected Results: Discount recalculated dynamically; cart total updated.  
Negative Scenarios: Discount not updated after quantity change.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-026  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Apply a valid promo code.  
2. Proceed to checkout.  
Expected Results: Discount persists through checkout; order summary reflects discount.  
Negative Scenarios: Discount lost during checkout.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-027  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Apply a valid promo code.  
2. Log out and log back in.  
3. Check cart.  
Expected Results: Discount persists in cart after re-login.  
Negative Scenarios: Discount lost after session change.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-028  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Apply a valid promo code.  
2. Remove promo code.  
Expected Results: Discount is removed; cart total updated.  
Negative Scenarios: Discount remains after removal.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-029  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Apply a valid promo code.  
2. Apply a second promo code.  
Expected Results: Only one promo code can be active at a time; error message if not allowed.  
Negative Scenarios: Multiple promo codes applied simultaneously.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-030  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Apply a valid promo code.  
2. Attempt to edit applied promo code.  
Expected Results: User can edit or remove promo code as per business rules.  
Negative Scenarios: Unable to edit or remove code.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-031  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Apply a valid promo code.  
2. Abandon cart and return later.  
Expected Results: Discount persists if cart is saved; otherwise, promo code must be reapplied.  
Negative Scenarios: Discount lost unexpectedly.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-032  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Apply a valid promo code.  
2. Change shipping address.  
Expected Results: Discount remains unless promo code is location-specific.  
Negative Scenarios: Discount removed due to address change.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-033  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Apply a valid promo code.  
2. Change payment method.  
Expected Results: Discount remains unless promo code is payment-method-specific.  
Negative Scenarios: Discount removed due to payment method change.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-034  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Apply a valid promo code.  
2. Attempt to checkout with ineligible payment method.  
Expected Results: Error message if promo code is not valid for selected payment method.  
Negative Scenarios: Discount applied incorrectly.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-035  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Apply a valid promo code.  
2. Attempt to checkout with ineligible shipping method.  
Expected Results: Error message if promo code is not valid for selected shipping method.  
Negative Scenarios: Discount applied incorrectly.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-036  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Apply a valid promo code.  
2. Attempt to checkout with ineligible billing country.  
Expected Results: Error message if promo code is not valid for selected country.  
Negative Scenarios: Discount applied incorrectly.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-037  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Apply a valid promo code.  
2. Attempt to checkout with ineligible shipping country.  
Expected Results: Error message if promo code is not valid for selected country.  
Negative Scenarios: Discount applied incorrectly.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-038  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Apply a valid promo code.  
2. Attempt to checkout with ineligible user group.  
Expected Results: Error message if promo code is not valid for user group.  
Negative Scenarios: Discount applied incorrectly.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-039  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Apply a valid promo code.  
2. Attempt to checkout with ineligible product combination.  
Expected Results: Error message if promo code is not valid for product combination.  
Negative Scenarios: Discount applied incorrectly.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-040  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Apply a valid promo code.  
2. Attempt to checkout with ineligible order value.  
Expected Results: Error message if promo code is not valid for order value.  
Negative Scenarios: Discount applied incorrectly.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-041  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Apply a valid promo code.  
2. Attempt to checkout with ineligible order type (e.g., subscription vs. one-time).  
Expected Results: Error message if promo code is not valid for order type.  
Negative Scenarios: Discount applied incorrectly.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-042  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Apply a valid promo code.  
2. Attempt to checkout with ineligible delivery date.  
Expected Results: Error message if promo code is not valid for selected delivery date.  
Negative Scenarios: Discount applied incorrectly.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-043  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Apply a valid promo code.  
2. Attempt to checkout with ineligible shipping speed.  
Expected Results: Error message if promo code is not valid for selected shipping speed.  
Negative Scenarios: Discount applied incorrectly.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-044  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Apply a valid promo code.  
2. Attempt to checkout with ineligible fulfillment method (e.g., pickup vs. delivery).  
Expected Results: Error message if promo code is not valid for fulfillment method.  
Negative Scenarios: Discount applied incorrectly.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-045  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Apply a valid promo code.  
2. Attempt to checkout with ineligible customer segment.  
Expected Results: Error message if promo code is not valid for customer segment.  
Negative Scenarios: Discount applied incorrectly.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-046  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Apply a valid promo code.  
2. Attempt to checkout with ineligible device type (e.g., mobile vs. desktop).  
Expected Results: Error message if promo code is not valid for device type.  
Negative Scenarios: Discount applied incorrectly.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-047  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Apply a valid promo code.  
2. Attempt to checkout with ineligible browser.  
Expected Results: Error message if promo code is not valid for browser.  
Negative Scenarios: Discount applied incorrectly.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-048  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Apply a valid promo code.  
2. Attempt to checkout with ineligible operating system.  
Expected Results: Error message if promo code is not valid for OS.  
Negative Scenarios: Discount applied incorrectly.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-049  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Apply a valid promo code.  
2. Attempt to checkout with ineligible language/locale.  
Expected Results: Error message if promo code is not valid for language/locale.  
Negative Scenarios: Discount applied incorrectly.  
Traceability: https://jira.example.com/browse/KAN-9
---
Test Case ID: KAN-9-TC-050  
Preconditions: User is logged in; cart contains items; promo code field is visible.  
Steps:  
1. Attempt to apply promo code during system downtime or maintenance.  
Expected Results: User receives maintenance message; promo code not applied.  
Negative Scenarios: Promo code applied during downtime.  
Traceability: https://jira.example.com/browse/KAN-9
---
All actions have been logged for auditing. No sensitive information is present in this output.  
Test cases are structured for direct integration with QA tools and CI/CD pipelines.