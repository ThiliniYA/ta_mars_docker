📄 Project Mars — Manual Test Cases
Author: Thilini
Module: Authentication, Languages, Skills, Access Control
Type: Functional, Negative, Boundary, Destructive

## 1. Registration Test Cases
TC_PM_Login_001 – Register with valid details
Steps:

Navigate to Join page

Enter valid first name, last name, email, password, confirm password

Accept Terms & Conditions

Click Join

Expected Result:  
Account created successfully; user redirected to dashboard

Actual Result:  
Account created successfully; user redirected to dashboard

Status: PASS

TC_PM_Login_002 – Register without accepting Terms & Conditions
Expected: Join button disabled OR validation message displayed
Actual: Join button disabled; validation message displayed
Status: PASS

TC_PM_Login_003 – Register with all fields empty
Expected: Mandatory field validation displayed
Actual: Join button disabled; validation messages displayed
Status: PASS

TC_PM_Login_004 – Register with special characters in name fields
Expected: “Names must contain at least one letter”
Actual: Validation message displayed
Status: PASS

TC_PM_Login_005 – Register with extremely long name (>1000 chars)
Expected: Input length validation error
Actual: Account created successfully (Defect)
Status: FAIL

TC_PM_Login_006 – Register with one‑letter names
Expected: Minimum name length validation
Actual: Account created successfully (Defect)
Status: FAIL

TC_PM_Login_007 – Register with invalid email format
Expected: Email format validation error
Actual: Account created; weak validation (Defect)
Status: FAIL

TC_PM_Login_008 – Register with existing email
Expected: “This email has already been used”
Actual: Duplicate email message displayed
Status: PASS

TC_PM_Login_009 – Register with extremely long email (>1000 chars)
Expected: Email length validation error
Actual: Account created; weak validation (Defect)
Status: FAIL

TC_PM_Login_010 – Register with very short email
Expected: Email format validation error
Actual: Account created; weak validation (Defect)
Status: FAIL

TC_PM_Login_011 – Register with extremely long password (>1000 chars)
Expected: Password length validation error
Actual: Account created successfully (Defect)
Status: FAIL

TC_PM_Login_012 – Register with short password (<6 chars)
Expected: “Password must be at least 6 characters”
Actual: Validation message displayed
Status: PASS

TC_PM_Login_013 – Register with weak password
Expected: Password strength validation error
Actual: Account created successfully (Defect)
Status: FAIL

TC_PM_Login_014 – Register without confirm password
Expected: “Does not match password”
Actual: Validation message displayed
Status: PASS

## 2. Login Test Cases
TC_PM_SignIn_001 – Login with valid email & password
Expected: User logged in and redirected to dashboard
Actual: User logged in successfully
Status: PASS

TC_PM_SignIn_002 – Login with valid email & invalid password
Expected: “Invalid password”
Actual: “Invalid password” message displayed
Status: PASS

TC_PM_SignIn_003 – Login with valid email & empty password
Expected: “Password must be at least 6 characters”
Actual: Validation message displayed
Status: PASS

TC_PM_SignIn_004 – Login with invalid email & valid password
Expected: “Invalid username”
Actual: Validation message displayed
Status: PASS

TC_PM_SignIn_005 – Login with empty email & valid password
Expected: “Please enter a valid email address”
Actual: Validation message displayed
Status: PASS

TC_PM_SignIn_006 – Login with invalid email & invalid password
Expected: “Invalid username or password”
Actual: Validation message displayed
Status: PASS

TC_PM_SignIn_007 – Login with both fields empty
Expected: Email & password validation messages
Actual: Both validation messages displayed
Status: PASS

TC_PM_SignIn_008 – Login with multiple emails entered
Expected: Email format validation error
Actual: Validation message displayed
Status: PASS

TC_PM_SignIn_009 – Verify Forgot Password link
Expected: Redirect to verification email page
Actual: Redirect successful
Status: PASS

TC_PM_SignIn_010 – Verify password reset email is received
Expected: Recovery email delivered
Actual: No email received (Defect)
Status: FAIL

## 3. Language Feature Test Cases
TC_PM_Language_001 – Add new language
Expected: Language added with selected level
Actual: Language added successfully
Status: PASS

TC_PM_Language_002 – Add duplicate language
Expected: “This language already exists”
Actual: Duplicate validation displayed
Status: PASS

TC_PM_Language_003 – Add duplicate language with different level
Expected: Duplicate validation
Actual: “Duplicated data” displayed
Status: PASS

TC_PM_Language_004 – Add language without selecting level
Expected: Validation error
Actual: “Please enter language and level”
Status: PASS

TC_PM_Language_005 – Add language with empty name
Expected: Validation error
Actual: Validation message displayed
Status: PASS

TC_PM_Language_006 – Add language with both fields empty
Expected: Validation error
Actual: Validation message displayed
Status: PASS

TC_PM_Language_007 – Add language with extremely long name (>1000 chars)
Expected: Length validation error
Actual: Language added successfully (Defect)
Status: FAIL

TC_PM_Language_008 – Delete existing language
Expected: Language removed
Actual: Language removed successfully
Status: PASS

TC_PM_Language_009 – Edit existing language level
Expected: Updated level displayed
Actual: Level updated successfully
Status: PASS

TC_PM_Language_010 – Add different language
Expected: Language added successfully
Actual: Language added successfully
Status: PASS

## 4. Skills Feature Test Cases
TC_PM_Skills_001 – Add new skill
Expected: Skill added with selected level
Actual: Skill added successfully
Status: PASS

TC_PM_Skills_002 – Add duplicate skill
Expected: Duplicate validation
Actual: Duplicate validation displayed
Status: PASS

TC_PM_Skills_003 – Add skill with empty name
Expected: Validation error
Actual: Validation message displayed
Status: PASS

TC_PM_Skills_004 – Add skill with empty level
Expected: Validation error
Actual: Validation message displayed
Status: PASS

TC_PM_Skills_005 – Add skill with both fields empty
Expected: Validation error
Actual: Validation message displayed
Status: PASS

TC_PM_Skills_006 – Add new skill with different level
Expected: Skill added successfully
Actual: Skill added successfully
Status: PASS

TC_PM_Skills_007 – Delete existing skill
Expected: Skill removed
Actual: Skill removed successfully
Status: PASS

TC_PM_Skills_009 – Edit existing skill
Expected: Skill updated
Actual: Skill updated successfully
Status: PASS

TC_PM_Skills_010 – Add skill with extremely long name (>100 chars)
Expected: Length validation error
Actual: Skill added successfully (Defect)
Status: FAIL

## 5. Authentication & Access Control
TC_PM_Auth_001 – Access profile without signing in
Expected: Redirect to login page
Actual: Redirect occurs after session expires
Status: PARTIAL PASS

TC_PM_Auth_002 – Access Skills page without signing in
Expected: Redirect to login page
Actual: Redirect occurs after session expires
Status: PARTIAL PASS

TC_PM_Auth_003 – Access Languages page without signing in
Expected: Redirect to login page
Actual: Redirect occurs after session expires
Status: PARTIAL PASS
