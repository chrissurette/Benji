# Benji - Deliverable 5

This repository contains the Deliverable 5 submission package for Benji, an internal payroll management system for a STEM education center.

## Deliverable 5 Files

- Final Word document: `deliverable-5/Benji_Deliverable5_UXD_Prototype_Testing.docx`
- Functional test cases: `deliverable-5/functional_test_cases.csv`
- Presentation script: `deliverable-5/presentation_script.md`
- Prototype: `deliverable-5/prototype/index.html`
- User journey summary: `deliverable-5/user_journey_map.md`
- Testing results summary: `deliverable-5/testing_results_summary.md`
- Team contributions: `deliverable-5/team_contributions.md`
- Change log: `deliverable-5/change_log.md`

## Prototype Demo Accounts

| Role | Email | Password |
|---|---|---|
| Employee | `emma.employee@benji.test` | `Employee#123` |
| Admin | `admin.payroll@benji.test` | `Admin#123` |

## Recommended Demo Flow

1. Open `deliverable-5/prototype/index.html` in a browser.
2. Log in as the employee.
3. Submit a time entry from the Log Hours screen.
4. Confirm the entry appears as `PENDING` in My Timesheets.
5. Log out and use the admin login.
6. Open the Review Queue and approve the pending entry.
7. Open Reports, generate the payroll report, and use Export CSV / Print for output.
8. Click Finalize Pay Run to generate pay stubs from the approved entries.
9. Optionally manage employee records (add/edit/deactivate) from the Employees screen.
10. Log back in as the employee and confirm the entry shows `APPROVED` and the new pay stub appears.

Prototype data persists in the browser between reloads. Use the **Reset Demo Data** button on the login screen to restore the original demo scenario.

## Repository Purpose

This repository is scoped only to Deliverable 5: UXD, Prototyping & Testing. It includes the journey-map documentation, working prototype, functional testing evidence, and presentation support material required for submission.

## Canvas Submission Checklist

- Submit the compiled Word document from `deliverable-5/`.
- Submit the recorded presentation video on Canvas.
- Include this GitHub repository link so the grader can review the prototype, tests, commits, and merge history.
