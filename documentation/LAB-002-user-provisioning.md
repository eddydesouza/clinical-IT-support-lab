# LAB-002: Clinical User Provisioning and Access Control

## Objective

Configure and validate a fictional physician account in OpenEMR to demonstrate clinical user provisioning, authentication testing, and role-based access control (RBAC).

## Lab Environment

- EHR Application: OpenEMR
- Deployment: Docker
- Database: MySQL
- Healthcare Facility: Lake County Medical Center (fictional)
- Environment: Local development lab
- Test Account: Dr. James Wilson (`jwilson`)

## Configuration

Created a physician account with the following settings:

| Setting | Configuration |
|---|---|
| Username | jwilson |
| Provider Type | Attending Physician |
| Access Control | Physicians |
| Provider | Enabled |
| Calendar | Enabled |
| Portal | Disabled |
| Default Facility | Lake County Medical Center |
| Main Menu Role | Standard |
| Patient Menu Role | Standard |

Passwords are stored separately from the repository.

## Validation Tests

### UAT-001: Physician Authentication

**Objective:** Verify that a newly provisioned physician can authenticate successfully.

**Procedure:**
1. Created the physician account using OpenEMR administration.
2. Opened a separate private browser session.
3. Authenticated using the physician's credentials.

**Expected Result:** Successful authentication.

**Actual Result:** Dr. Wilson successfully logged into OpenEMR.

**Status:** PASSED

### UAT-002: Role-Based Menu Visibility

**Objective:** Compare the physician's available navigation options with those of the administrator.

**Expected Result:** The physician should not have the same administrative menu visibility as the administrator.

**Actual Result:** The physician account did not display the Admin or Modules menus available to the administrator.

**Status:** PASSED — Menu visibility only.

**Limitation:** Direct access to restricted administrative functions has not yet been tested.

### UAT-003: Clinical Workflow Access

**Objective:** Verify that the physician can access patient-related functions.

**Actual Result:** The physician could access the Patient menu, register a fictional patient, and create an outpatient encounter.

**Status:** PASSED — Tested functions only.

## Key Takeaways

This exercise demonstrated:

- Clinical user provisioning
- Role-based access configuration
- Authentication validation
- Comparison of role-specific application menus
- Clinical workflow access testing
- Documentation of expected and actual results

## Next Steps

- Test direct access restrictions for administrative functions.
- Provision additional fictional clinical and front-office users.
- Compare permissions across roles.
- Investigate and document simulated access-related incidents.

*All users, patient records, and healthcare organizations in this lab are fictional.*

