# OrangeHRM Functional Testing

## Project Overview
This QA project contains functional test cases, test execution results, bug reports and observations for the OrangeHRM Demo system (https://opensource-demo.orangehrmlive.com). The goal is to validate core HR functionalities with a focus on Leave management, My Info personal details, and Dashboard operations.

---

## Tools Used
- **Test Management:** Microsoft Excel
- **Bug Tracking:** Excel Bug Report
- **Browser:** Chrome (latest version)
- **OS:** Windows 11
- **Screenshot Tool:** Snipping Tool

---

## Test Environment
- **OS:** Windows 11
- **Browser:** Chrome (latest version)
- **URL:** https://opensource-demo.orangehrmlive.com
- **Credentials:** Username: Admin | Password: admin123
- **Test Type:** Manual functional testing

---

## Test Scope

**Modules Covered:**
- **Dashboard:** Widget display, navigation, quick launch items
- **My Info:** Personal details, contact details, emergency contacts, dependents, immigration, job, salary, report-to, qualifications, memberships
- **Leave:** Leave list, apply, my leave, add entitlements, employee entitlements, my leave entitlements, reports, configure, assign leave

**Functionalities Tested:**
- Field validations — mandatory fields, date validations, dropdowns
- Leave application flows — single-day, multi-day, partial days
- Leave assignment and approval workflow
- Status updates and action history
- Observations for unclear or demo-specific fields

---

## Test Summary

| Total Test Cases | Passed | Failed | Blocked | Pass Rate |
|---|---|---|---|---|
| 117 | 115 | 2 | 0 | 98.3% |

---

## Per Module Summary

| Module | Total | Passed | Failed | Blocked |
|---|---|---|---|---|
| Login | 6 | 6 | 0 | 0 |
| Dashboard | 23 | 23 | 0 | 0 |
| My Info - Personal Details | 12 | 10 | 2 | 0 |
| My Info - Contact Details | 3 | 3 | 0 | 0 |
| My Info - Emergency Contacts | 4 | 4 | 0 | 0 |
| My Info - Dependents | 4 | 4 | 0 | 0 |
| My Info - Immigration | 4 | 4 | 0 | 0 |
| My Info - Job | 3 | 3 | 0 | 0 |
| My Info - Salary | 1 | 1 | 0 | 0 |
| My Info - Report To | 1 | 1 | 0 | 0 |
| My Info - Qualifications | 7 | 7 | 0 | 0 |
| My Info - Memberships | 3 | 3 | 0 | 0 |
| Leave - Leave List | 7 | 7 | 0 | 0 |
| Leave - Apply | 9 | 9 | 0 | 0 |
| Leave - My Leave | 4 | 4 | 0 | 0 |
| Leave - Add Entitlements | 4 | 4 | 0 | 0 |
| Leave - Employee Entitlements | 4 | 4 | 0 | 0 |
| Leave - My Leave Entitlements | 2 | 2 | 0 | 0 |
| Leave - Reports | 3 | 3 | 0 | 0 |
| Leave - Configure | 8 | 8 | 0 | 0 |
| Leave - Assign Leave | 5 | 5 | 0 | 0 |
| **TOTAL** | **117** | **115** | **2** | **0** |

---

## Bug Report Summary

| Bug ID | Description | Severity | Priority |
|---|---|---|---|
| OHRM_BUG_001 | Date of Birth field accepts a future date | High | P1 (Medium) |
| OHRM_BUG_002 | License Expiry Date field accepts a past date | Medium | P1 (Medium) |

---

## Observations

| Observation ID | Description |
|---|---|
| OHRM_OBS_001 | Unclear purpose of Test_Field in Custom Fields section under Personal Details |

---

## Test Case Structure
Each test case includes:
- TC ID
- Test Scenario
- Pre-requisites
- Test Steps
- Test Data
- Expected Result

---

## Bug Report Structure
Each bug report includes:
- Bug ID
- Title/Description
- Steps to Reproduce
- Expected Result
- Actual Result
- Severity
- Priority
- Screenshot

Failed test cases link to their corresponding bug report via Bug ID.

---

## Test Approach
- Manual functional testing on the public OrangeHRM demo site
- Positive, negative and edge cases included
- Focus on business rule validation such as leave balance and date restrictions

---

## Repository Structure
```
OrangeHRM-Testing
├── README.md
└── OrangeHRM/
    ├── OrangeHRM_TestCases.xlsx
    ├── OrangeHRM_TestExecutionResults.xlsx
    ├── OrangeHRM_BugReport.xlsx
    └── Screenshots/
        ├── OHRM_BUG_001_Future_Date_Accepted.png
        ├── OHRM_BUG_002_Past_Date_Accepted.png
        └── OHRM_OBS_001_Test_Field.png
```

---

## Notes
- Forgot Password workflow cannot be fully tested due to demo email restrictions
- Some default demo fields such as Test_Field are unclear in purpose — logged as an observation
- Leave balance behaviour allows negative balance which may be demo-specific
- License Expiry Date accepts past dates — this may be intentional to allow recording of historical licence data but flagged as a bug due to potential for misleading data in an HR context
