# Bug Report - GemNet Application

## Bug #1

### Basic Info
- **Bug ID**: BUG-001
- **Module**: Registration (REG)
- **Test Case**: REG-003
- **Severity**: Medium
- **Status**: Open
- **Date Reported**: Current Testing Cycle

### Title
Email validation not showing error message

### Description
When user enters an invalid email format, the system should display an error message. However, the error message is not appearing on the screen.

### Steps to Reproduce
1. Go to Registration page
2. Click on Email field
3. Enter invalid email: `iit21089gmail.com` (missing @ symbol)
4. Submit the form
5. Expected: Error message should show
6. Actual: No error message shown

### Expected Behavior
System should display error message: "Please enter a valid email address"

### Actual Behavior
Form accepts invalid email without showing any error

### Test Data Used
- Invalid Email: `iit21089gmail.com`

### Environment
- Application: GemNet Staging
- Browser: [Not specified in test data]
- OS: [Not specified in test data]

### Affected Feature
User Registration Form - Email Field Validation

### Priority
Medium - Email validation is important for data integrity

---

## Bug #2

### Basic Info
- **Bug ID**: BUG-002
- **Module**: Listings (LIST)
- **Test Case**: LIST-004
- **Severity**: High
- **Status**: Open
- **Date Reported**: Current Testing Cycle

### Title
Edit listing functionality not working

### Description
When seller tries to edit an existing listing, the changes are not being saved. The edit function appears to be broken.

### Steps to Reproduce
1. Login as Seller account
2. Go to My Listings section
3. Click on existing listing
4. Click Edit button
5. Update listing data (Price, Description, etc.)
6. Submit changes
7. Expected: Changes should be saved and visible
8. Actual: Edit does not work

### Expected Behavior
- Form should open for editing
- Changes should be saved when user clicks Save/Submit
- Updated listing should be visible in marketplace

### Actual Behavior
- Edit functionality does not work
- Changes are not saved

### Impact
Sellers cannot update their listings after creation. This is a significant feature limitation.

### Affected Feature
Listing Management - Edit Function

### Priority
High - Core feature for sellers affected

### Test Data Used
- Listing Type: Natural Unheated Pink Sapphire
- Original Data: Name, Price, Weight, Color, Shape, Origin, Treatment

---

## Summary Table

| Bug ID | Module | Test Case | Title | Severity | Status |
|--------|--------|-----------|-------|----------|--------|
| BUG-001 | Registration | REG-003 | Email validation error not showing | Medium | Open |
| BUG-002 | Listings | LIST-004 | Edit listing not working | High | Open |

---

## Recommendations

### For BUG-001 (Email Validation)
- Check email validation logic in Registration form
- Add client-side validation
- Add server-side validation
- Test with various invalid email formats

### For BUG-002 (Edit Listing)
- Check edit endpoint functionality
- Verify form submission handling
- Test database update operations
- Ensure proper permissions for seller to edit

---

## Notes
- Both bugs need to be fixed before production release
- BUG-002 has higher priority due to impact on core seller functionality
- Email validation can be addressed quickly
