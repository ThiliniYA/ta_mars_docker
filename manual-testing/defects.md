Project Mars — Defect Log (Manual Testing)
Author: Thilini
Module: Authentication, Languages, Skills, Access Control
Testing Type: Functional, Negative, Boundary, Destructive
Environment: Localhost (Docker) – http://localhost:5003

## Defect Summary
Defect ID	Area	Severity	Status
DEF_PM_001	Registration – Name field	Medium	Open
DEF_PM_002	Registration – Email validation	High	Open
DEF_PM_003	Registration – Long email accepted	High	Open
DEF_PM_004	Registration – Weak password accepted	High	Open
DEF_PM_005	Registration – Long password accepted	Medium	Open
DEF_PM_006	Forgot Password – No email received	Critical	Open
DEF_PM_007	Languages – Long name accepted	Medium	Open
DEF_PM_008	Skills – Long name accepted	Medium	Open
DEF_PM_009	Authentication – Session persists after closing tab	Medium	Open


## Detailed Defects
DEF_PM_001 – System accepts extremely long names (>1000 characters)
Module: Registration
Severity: Medium
Steps to Reproduce:

Navigate to Join page

Enter 1000+ characters in First Name and Last Name

Enter valid email and password

Click Join

Expected Result:  
Validation error for maximum character limit

Actual Result:  
Account created successfully

Status: Open
Notes: Input length validation is missing for name fields

DEF_PM_002 – Weak email validation (invalid formats accepted)
Module: Registration
Severity: High
Steps:

Enter invalid email formats (e.g., 5555@55.com, t@g.com)

Complete the other fields correctly

Click Join

Expected:  
Email format validation error

Actual:  
Account created successfully; only minimal validation applied

Status: Open
Notes: Email regex too weak

DEF_PM_003 – Extremely long email (>1000 chars) accepted
Module: Registration
Severity: High
Steps:

Enter email with 1000+ characters

Submit registration

Expected:  
Validation error

Actual:  
Account created successfully

Status: Open

DEF_PM_004 – Weak passwords accepted (no complexity rules)
Module: Registration
Severity: High
Steps:

Enter the password with only emojis, numbers, or special characters

Submit registration

Expected:  
Password strength validation

Actual:  
Account created successfully

Status: Open

DEF_PM_005 – Extremely long password (>1000 chars) accepted
Module: Registration
Severity: Medium
Steps:

Enter password with 1000+ characters

Submit registration

Expected:  
Validation error

Actual:  
Account created successfully

Status: Open

DEF_PM_006 – Forgot Password: No recovery email received
Module: Authentication
Severity: Critical
Steps:

Click “Forgot Password”

Enter registered email

Click “Send Verification Email”

Expected:  
Recovery email received in inbox

Actual:  
Success message displayed but no email received

Status: Open
Notes: Email service may not be configured or failing silently

DEF_PM_007 – Languages: System accepts extremely long language names
Module: Languages
Severity: Medium
Steps:

Add a language with 1000+ characters

Click Add

Expected:  
Validation error

Actual:  
Language added successfully

Status: Open

DEF_PM_008 – Skills: System accepts extremely long skill names
Module: Skills
Severity: Medium
Steps:

Add a skill with 100+ characters

Click Add

Expected:  
Validation error

Actual:  
Skill added successfully

Status: Open

DEF_PM_009 – Session persists after closing browser tab
Module: Authentication / Access Control
Severity: Medium
Steps:

Log in

Close browser tab without logging out

Reopen profile URL

Expected:  
Redirect to login page

Actual:  
Page loads partially; some data missing but no redirect

Status: Open
Notes: Session timeout or cookie handling issue
