# Project Mars – Manual Testing Documentation

## 📌 Overview
This folder contains the manual test cases, test execution results, and identified defects for Project Mars, focusing on:

- User Authentication (Join & Login)
- Languages Feature
- Skills Feature
- Access Control & Authorization

These test cases were created based on the user stories and acceptance criteria provided in the Mars Onboarding Task.

---

## 🎯 Objectives
- Analyze requirements and create comprehensive manual test cases  
- Cover positive, negative, edge-case, and destructive scenarios  
- Validate functionality of Languages and Skills modules  
- Verify authentication and access control  
- Document defects found during testing  
- Provide a structured, professional QA deliverable for GitHub

---

## 📂 Folder Structure

manual-testing/
│
├── README.md                # Documentation (this file)
├── test-cases.md            # Full list of 40+ test cases
├── defects.md               # Defects identified during manual testing
└── screenshots/             # (Optional) Evidence of test execution



---

## 🧪 Test Coverage Summary

### ✔ 1. Registration
Covers:
- Valid registration  
- Missing fields  
- Invalid formats  
- Weak passwords  
- Duplicate accounts  
- Boundary testing (1000+ characters)

### ✔ 2. Login
Covers:
- Valid login  
- Invalid credentials  
- Empty fields  
- Forgot password  
- Email verification flow  

### ✔ 3. Languages Feature
Covers:
- Add language  
- Edit language  
- Delete language  
- Duplicate prevention  
- Missing fields  
- Boundary testing (long names)

### ✔ 4. Skills Feature
Covers:
- Add skill  
- Edit skill  
- Delete skill  
- Duplicate prevention  
- Missing fields  
- Boundary testing (long names)

### ✔ 5. Authentication & Access Control
Covers:
- Accessing profile without login  
- Direct URL access  
- Session handling behavior  

---

## Test Case Format
All test cases follow a consistent structure:

- Test Scenario ID  
- Test Case ID  
- Description  
- Pre-conditions  
- Test Steps  
- Expected Result  
- Actual Result  
- Status  
- Comments  

This format ensures clarity, traceability, and easy conversion into automation later.

---

## 🐞 Defects Identified
A separate file (`defects.md`) documents issues found during manual testing, including:

- Weak email validation  
- Weak password validation  
- Missing character limits  
- Duplicate skill handling inconsistency  
- Email verification not sending actual emails  
- Session persistence issues  

Each defect includes:
- Steps to reproduce  
- Expected vs actual behavior  
- Severity  
- Suggested fix  

---

## 📄 Related Files
- **test-cases.md** → Full list of 40+ test cases  
- **defects.md** → All defects discovered during testing  
- **screenshots/** → Optional evidence folder  

---

## 🚀 Next Steps (Automation Phase)
These manual test cases will be used to create:

- BDD `.feature` files  
- Step definitions using Reqnroll  
- Page Object Model classes  
- Selenium WebDriver tests  
- NUnit assertions  

This ensures a smooth transition from manual to automated testing.

---

## 👤 Author
**Thilini**  
Manual & Automation QA | MVP Studio Onboarding Program
