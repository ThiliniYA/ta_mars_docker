📄 Project Mars – Manual Test Cases
Author: Thilini
Module: Authentication, Languages, Skills, Access Control
Total Test Cases: 40+
Type: Functional, Negative, Boundary, Destructive

## 1. Registration Test Cases
TC_PM_Login_001 – Register with valid details
Steps:

Navigate to Join page

Enter valid first name, last name, email, password, confirm password

Accept Terms & Conditions

Click Join
Expected: Account created successfully; user redirected to dashboard

TC_PM_Login_002 – Register without accepting Terms & Conditions
Expected: Join button disabled OR validation message displayed

TC_PM_Login_003 – Register with all fields empty
Expected: Mandatory field validation displayed

TC_PM_Login_004 – Register with special characters in name fields
Expected: “Names must contain at least one letter”

TC_PM_Login_005 – Register with extremely long name (>1000 chars)
Expected: Input length validation error

TC_PM_Login_006 – Register with one‑letter names
Expected: Minimum name length validation

TC_PM_Login_007 – Register with invalid email format
Expected: Email format validation error

TC_PM_Login_008 – Register with existing email
Expected: “This email has already been used”

TC_PM_Login_009 – Register with extremely long email (>1000 chars)
Expected: Email length validation error

TC_PM_Login_010 – Register with very short email
Expected: Email format validation error

TC_PM_Login_011 – Register with extremely long password (>1000 chars)
Expected: Password length validation error

TC_PM_Login_012 – Register with short password (<6 chars)
Expected: “Password must be at least 6 characters”

TC_PM_Login_013 – Register with weak password
Expected: Password strength validation error

TC_PM_Login_014 – Register without confirm password
Expected: “Does not match password”

## 2. Login Test Cases
TC_PM_SignIn_001 – Login with valid email & password
Expected: User logged in and redirected to dashboard

TC_PM_SignIn_002 – Login with valid email & invalid password
Expected: “Invalid password”

TC_PM_SignIn_003 – Login with valid email & empty password
Expected: “Password must be at least 6 characters”

TC_PM_SignIn_004 – Login with invalid email & valid password
Expected: “Invalid username”

TC_PM_SignIn_005 – Login with empty email & valid password
Expected: “Please enter a valid email address”

TC_PM_SignIn_006 – Login with invalid email & invalid password
Expected: “Invalid username or password”

TC_PM_SignIn_007 – Login with both fields empty
Expected: Email & password validation messages

TC_PM_SignIn_008 – Login with multiple emails entered
Expected: Email format validation error

TC_PM_SignIn_009 – Verify Forgot Password link
Expected: Redirect to verification email page

TC_PM_SignIn_010 – Verify password reset email is received
Expected: Recovery email delivered to inbox

## 3. Language Feature Test Cases
TC_PM_Language_001 – Add new language
Expected: Language added with selected level

TC_PM_Language_002 – Add duplicate language
Expected: “This language already exists”

TC_PM_Language_003 – Add duplicate language with different level
Expected: Duplicate validation triggered

TC_PM_Language_004 – Add language without selecting level
Expected: “Please enter language and level”

TC_PM_Language_005 – Add language with empty name
Expected: Validation error

TC_PM_Language_006 – Add language with both fields empty
Expected: Validation error

TC_PM_Language_007 – Add language with extremely long name (>1000 chars)
Expected: Length validation error

TC_PM_Language_008 – Delete existing language
Expected: Language removed from list

TC_PM_Language_009 – Edit existing language level
Expected: Updated level displayed

TC_PM_Language_010 – Add different language with valid level
Expected: Language added successfully

## 4. Skills Feature Test Cases
TC_PM_Skills_001 – Add new skill
Expected: Skill added with selected level

TC_PM_Skills_002 – Add duplicate skill
Expected: “This skill already exists”

TC_PM_Skills_003 – Add skill with empty name
Expected: Validation error

TC_PM_Skills_004 – Add skill with empty level
Expected: Validation error

TC_PM_Skills_005 – Add skill with both fields empty
Expected: Validation error

TC_PM_Skills_006 – Add new skill with different level
Expected: Skill added successfully

TC_PM_Skills_007 – Delete existing skill
Expected: Skill removed from list

TC_PM_Skills_009 – Edit existing skill level
Expected: Skill updated successfully

TC_PM_Skills_010 – Add skill with extremely long name (>100 chars)
Expected: Length validation error

## 5. Authentication & Access Control Test Cases
TC_PM_Auth_001 – Access profile without signing in
Expected: Redirect to login page

TC_PM_Auth_002 – Access Skills page without signing in
Expected: Redirect to login page

TC_PM_Auth_003 – Access Languages page without signing in
Expected: Redirect to login page
