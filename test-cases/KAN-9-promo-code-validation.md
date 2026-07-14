# Test Cases for Story: Implement Promo Code Validation and Dynamic Cart Discount Calculation

## Traceability: https://jira.example.com/browse/KAN-9

---

### TC-KAN-9-001
- Preconditions: User is logged in and has at least one item in the cart
- Steps:
  1. Navigate to the cart page
  2. Enter a valid promo code
  3. Click "Apply"
- Expected Results: Discount is applied to the cart total as per promo code rules
- Negative Scenarios: Entering an expired promo code, entering a code not applicable to cart items

---

### TC-KAN-9-002
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter an invalid promo code
  2. Click "Apply"
- Expected Results: Error message is displayed, no discount applied
- Negative Scenarios: Entering special characters, empty input

---

### TC-KAN-9-003
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code that has already been used by the user
  2. Click "Apply"
- Expected Results: Error message indicating code already used
- Negative Scenarios: Attempting to reuse a single-use code

---

### TC-KAN-9-004
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code that is not applicable to the current cart items
  2. Click "Apply"
- Expected Results: Error message indicating code not applicable
- Negative Scenarios: Code for electronics applied to a cart with only clothing

---

### TC-KAN-9-005
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code with minimum cart value requirement
  2. Ensure cart value is below minimum
  3. Click "Apply"
- Expected Results: Error message indicating minimum cart value not met
- Negative Scenarios: Cart value just below threshold

---

### TC-KAN-9-006
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a valid promo code
  2. Remove an item from the cart so that the cart value drops below the promo code threshold
- Expected Results: Discount is removed, user is notified
- Negative Scenarios: Removing multiple items at once

---

### TC-KAN-9-007
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a valid promo code
  2. Add more items to the cart
- Expected Results: Discount recalculates dynamically based on new cart total
- Negative Scenarios: Adding items that are not eligible for discount

---

### TC-KAN-9-008
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a valid promo code
  2. Change the quantity of an item in the cart
- Expected Results: Discount recalculates based on updated quantity
- Negative Scenarios: Reducing quantity below eligibility

---

### TC-KAN-9-009
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a valid promo code
  2. Proceed to checkout
- Expected Results: Discount is reflected in the order summary and final payment
- Negative Scenarios: Discount not carried over to checkout

---

### TC-KAN-9-010
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a valid promo code
  2. Log out and log back in
  3. Return to cart
- Expected Results: Discount persists if cart is unchanged
- Negative Scenarios: Cart is cleared on logout

---

### TC-KAN-9-011
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a valid promo code
  2. Remove the promo code
- Expected Results: Discount is removed, cart total updates
- Negative Scenarios: Removing code after checkout

---

### TC-KAN-9-012
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a valid promo code
  2. Enter another valid promo code
- Expected Results: Only one promo code can be applied at a time
- Negative Scenarios: Attempting to stack multiple codes

---

### TC-KAN-9-013
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code with a maximum discount cap
  2. Ensure cart value exceeds cap
- Expected Results: Discount does not exceed maximum allowed
- Negative Scenarios: Cap not enforced

---

### TC-KAN-9-014
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code with a percentage discount
  2. Verify discount calculation
- Expected Results: Discount is calculated as a percentage of eligible items
- Negative Scenarios: Incorrect percentage applied

---

### TC-KAN-9-015
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code with a fixed amount discount
  2. Verify discount calculation
- Expected Results: Discount is subtracted as a fixed amount
- Negative Scenarios: Discount exceeds cart total

---

### TC-KAN-9-016
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code with product-specific eligibility
  2. Add and remove eligible/ineligible products
- Expected Results: Discount applies only to eligible products
- Negative Scenarios: Discount applied to ineligible products

---

### TC-KAN-9-017
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code with a usage limit per user
  2. Attempt to use code after limit reached
- Expected Results: Error message, code cannot be reused
- Negative Scenarios: Limit not enforced

---

### TC-KAN-9-018
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code with a global usage limit
  2. Attempt to use code after limit reached
- Expected Results: Error message, code cannot be used
- Negative Scenarios: Code still applies after limit

---

### TC-KAN-9-019
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code with a start and end date
  2. Attempt to use code before start date
  3. Attempt to use code after end date
- Expected Results: Error message for invalid timing
- Negative Scenarios: Code applies outside valid period

---

### TC-KAN-9-020
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code with a minimum quantity requirement
  2. Add/remove items to meet/not meet requirement
- Expected Results: Discount applies only when requirement met
- Negative Scenarios: Discount applies with insufficient quantity

---

### TC-KAN-9-021
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code with a category restriction
  2. Add items from different categories
- Expected Results: Discount applies only to specified category
- Negative Scenarios: Discount applies to all categories

---

### TC-KAN-9-022
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code with a brand restriction
  2. Add items from different brands
- Expected Results: Discount applies only to specified brand
- Negative Scenarios: Discount applies to all brands

---

### TC-KAN-9-023
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code with a product exclusion
  2. Add excluded products
- Expected Results: Discount does not apply to excluded products
- Negative Scenarios: Discount applies to excluded products

---

### TC-KAN-9-024
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code with a shipping discount
  2. Proceed to checkout
- Expected Results: Shipping cost is reduced as per promo code
- Negative Scenarios: Shipping discount not applied

---

### TC-KAN-9-025
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code with a free gift offer
  2. Verify free gift is added to cart
- Expected Results: Free gift appears in cart
- Negative Scenarios: Gift not added, gift added multiple times

---

### TC-KAN-9-026
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code with a BOGO (Buy One Get One) offer
  2. Add eligible items
- Expected Results: Free item is added as per offer
- Negative Scenarios: Free item not added, incorrect item added

---

### TC-KAN-9-027
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code with a tiered discount (e.g., 10% off for $100+, 20% off for $200+)
  2. Adjust cart value to cross thresholds
- Expected Results: Discount updates as per tier
- Negative Scenarios: Incorrect tier applied

---

### TC-KAN-9-028
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Refresh the page
- Expected Results: Discount persists after refresh
- Negative Scenarios: Discount lost on refresh

---

### TC-KAN-9-029
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Open cart in a new browser/tab
- Expected Results: Discount is consistent across sessions
- Negative Scenarios: Discount not reflected in new tab

---

### TC-KAN-9-030
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Clear browser cookies
  3. Return to cart
- Expected Results: Discount is removed if session is lost
- Negative Scenarios: Discount persists incorrectly

---

### TC-KAN-9-031
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply the same code multiple times
- Expected Results: Code can only be applied once
- Negative Scenarios: Multiple discounts applied

---

### TC-KAN-9-032
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply a different code after one is already applied
- Expected Results: Previous code is replaced or error shown
- Negative Scenarios: Both codes applied

---

### TC-KAN-9-033
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply a code with leading/trailing spaces
- Expected Results: Spaces are trimmed, code is validated
- Negative Scenarios: Code rejected due to spaces

---

### TC-KAN-9-034
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code in lowercase/uppercase
- Expected Results: Code is case-insensitive
- Negative Scenarios: Code rejected due to case sensitivity

---

### TC-KAN-9-035
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with special characters
- Expected Results: Code is validated, error for invalid format
- Negative Scenarios: Code accepted with invalid characters

---

### TC-KAN-9-036
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with empty input
- Expected Results: Error message for empty input
- Negative Scenarios: Code accepted as blank

---

### TC-KAN-9-037
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with SQL injection or script
- Expected Results: Input is sanitized, error shown
- Negative Scenarios: Security vulnerability

---

### TC-KAN-9-038
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with XSS payload
- Expected Results: Input is sanitized, no script execution
- Negative Scenarios: XSS vulnerability

---

### TC-KAN-9-039
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with Unicode/emoji characters
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with invalid characters

---

### TC-KAN-9-040
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with maximum allowed length
- Expected Results: Code is accepted if within limit
- Negative Scenarios: Code rejected due to length

---

### TC-KAN-9-041
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code exceeding maximum length
- Expected Results: Error for exceeding length
- Negative Scenarios: Code accepted despite length

---

### TC-KAN-9-042
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with non-ASCII characters
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with non-ASCII

---

### TC-KAN-9-043
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with whitespace in the middle
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with spaces

---

### TC-KAN-9-044
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with tab/newline characters
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with control characters

---

### TC-KAN-9-045
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with leading zeros
- Expected Results: Code is validated correctly
- Negative Scenarios: Code rejected due to leading zeros

---

### TC-KAN-9-046
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with trailing zeros
- Expected Results: Code is validated correctly
- Negative Scenarios: Code rejected due to trailing zeros

---

### TC-KAN-9-047
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with mixed alphanumeric and symbols
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with symbols

---

### TC-KAN-9-048
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with only numbers
- Expected Results: Code is validated as per rules
- Negative Scenarios: Code rejected due to format

---

### TC-KAN-9-049
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with only letters
- Expected Results: Code is validated as per rules
- Negative Scenarios: Code rejected due to format

---

### TC-KAN-9-050
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with mixed case
- Expected Results: Code is case-insensitive
- Negative Scenarios: Code rejected due to case

---

### TC-KAN-9-051
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with duplicate characters
- Expected Results: Code is validated as per rules
- Negative Scenarios: Code rejected due to duplicates

---

### TC-KAN-9-052
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with palindromic pattern
- Expected Results: Code is validated as per rules
- Negative Scenarios: Code rejected due to pattern

---

### TC-KAN-9-053
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with sequential characters
- Expected Results: Code is validated as per rules
- Negative Scenarios: Code rejected due to sequence

---

### TC-KAN-9-054
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with random characters
- Expected Results: Code is validated as per rules
- Negative Scenarios: Code rejected due to randomness

---

### TC-KAN-9-055
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with known test values
- Expected Results: Code is validated as per rules
- Negative Scenarios: Code rejected due to test value

---

### TC-KAN-9-056
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with whitespace only
- Expected Results: Error for empty input
- Negative Scenarios: Code accepted as blank

---

### TC-KAN-9-057
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with HTML tags
- Expected Results: Input is sanitized, error for invalid format
- Negative Scenarios: HTML rendered in UI

---

### TC-KAN-9-058
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with JSON format
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted as JSON

---

### TC-KAN-9-059
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with XML format
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted as XML

---

### TC-KAN-9-060
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with URL encoding
- Expected Results: Code is decoded and validated
- Negative Scenarios: Code rejected due to encoding

---

### TC-KAN-9-061
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with base64 encoding
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted as base64

---

### TC-KAN-9-062
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with binary format
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted as binary

---

### TC-KAN-9-063
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with hexadecimal format
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted as hex

---

### TC-KAN-9-064
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with octal format
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted as octal

---

### TC-KAN-9-065
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with scientific notation
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted as scientific notation

---

### TC-KAN-9-066
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with currency symbols
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with currency symbols

---

### TC-KAN-9-067
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with mathematical symbols
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with math symbols

---

### TC-KAN-9-068
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with punctuation marks
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with punctuation

---

### TC-KAN-9-069
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with escape characters
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with escape characters

---

### TC-KAN-9-070
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with accented characters
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with accents

---

### TC-KAN-9-071
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with diacritics
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with diacritics

---

### TC-KAN-9-072
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with invisible characters
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with invisible characters

---

### TC-KAN-9-073
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with right-to-left text
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with RTL text

---

### TC-KAN-9-074
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with left-to-right override
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with LTR override

---

### TC-KAN-9-075
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with bidirectional text
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with bidi text

---

### TC-KAN-9-076
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with surrogate pairs
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with surrogate pairs

---

### TC-KAN-9-077
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with combining characters
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with combining characters

---

### TC-KAN-9-078
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with ligatures
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with ligatures

---

### TC-KAN-9-079
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with rare Unicode blocks
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with rare Unicode

---

### TC-KAN-9-080
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with control characters
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with control characters

---

### TC-KAN-9-081
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with whitespace at various positions
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with misplaced whitespace

---

### TC-KAN-9-082
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with invisible zero-width space
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with zero-width space

---

### TC-KAN-9-083
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with surrogate pairs and combining marks
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with complex Unicode

---

### TC-KAN-9-084
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with emoji
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with emoji

---

### TC-KAN-9-085
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with CJK characters
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with CJK

---

### TC-KAN-9-086
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with Arabic script
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with Arabic

---

### TC-KAN-9-087
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with Cyrillic script
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with Cyrillic

---

### TC-KAN-9-088
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with Greek script
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with Greek

---

### TC-KAN-9-089
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with Devanagari script
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with Devanagari

---

### TC-KAN-9-090
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with Thai script
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with Thai

---

### TC-KAN-9-091
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with Hebrew script
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with Hebrew

---

### TC-KAN-9-092
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with Hangul script
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with Hangul

---

### TC-KAN-9-093
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with Armenian script
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with Armenian

---

### TC-KAN-9-094
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with Georgian script
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with Georgian

---

### TC-KAN-9-095
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with Ethiopic script
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with Ethiopic

---

### TC-KAN-9-096
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with Cherokee script
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with Cherokee

---

### TC-KAN-9-097
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with Canadian Aboriginal script
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with Canadian Aboriginal

---

### TC-KAN-9-098
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with Ogham script
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with Ogham

---

### TC-KAN-9-099
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with Runic script
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with Runic

---

### TC-KAN-9-100
- Preconditions: User is on the cart page with items in the cart
- Steps:
  1. Enter a promo code
  2. Attempt to apply code with random rare scripts
- Expected Results: Error for invalid format
- Negative Scenarios: Code accepted with rare scripts

---

All actions have been logged for auditing. No sensitive information is present in this output.
This output is structured for direct integration with QA tools or CI/CD pipelines.
