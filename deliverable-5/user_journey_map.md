# Benji User Journey Map

This journey map summarizes the Deliverable 5 prototype workflow for Benji, an internal payroll management system.

## Primary Users

- Instructor / Tutor: submits hours and checks approval status.
- Program Supervisor: reviews submitted time entries.
- Payroll Admin: manages approval flow and payroll reports.
- CEO: needs confidence that payroll data is accurate and auditable.

## Implemented Journey

| Phase | User Action | UI Interaction | System Response | Prototype Screen |
|---|---|---|---|---|
| Access system | User enters credentials | Login form | Authenticates user and routes by role | SCR-01 Login |
| Employee dashboard | Employee reviews pay-period status | Summary cards and navigation buttons | Displays pending entries, approved hours, and activity | SCR-02 Employee Dashboard |
| Submit hours | Employee enters date, hours, program, and notes | Time entry form | Validates data and saves entry as pending | SCR-04 Time Entry Form |
| View status | Employee checks own entries | Timesheet table and status badges | Shows pending, approved, rejected, or flagged status | SCR-05 My Timesheets |
| Review queue | Admin opens submitted entries | Approval queue table and Review buttons | Loads pending entries for review | SCR-06 Timesheet Approval Queue |
| Record decision | Admin approves, rejects, or flags entry | Review modal, notes field, decision buttons | Updates entry status and records audit event | SCR-07 Timesheet Review |
| Payroll report | Admin generates payroll output | Report generator and payroll table | Calculates gross pay, deductions, net pay, and totals | SCR-12 Payroll Report |
| Report export | Admin downloads or prints the report | Export CSV and Print / Save PDF buttons | Produces a CSV file or print-ready report and records an audit event | SCR-12 Payroll Report |
| Pay run finalization | Admin finalizes the pay period | Finalize Pay Run button | Generates pay stubs per employee from approved entries not yet paid | SCR-12 → SCR-10 |
| Pay stub history | Employee reviews finalized pay | Pay stub table with deductions | Displays generated and historical pay stubs, newest first | SCR-10 Pay Stub History |
| Employee management | Admin maintains employee records | Add/Edit forms and Deactivate controls | Validates and saves records, blocks inactive employees from submitting hours | SCR-08 Employee Directory |

## Prototype Coverage

The prototype implements the complete journey from employee login through payroll report generation, report export, and pay-run finalization that feeds employee pay-stub history. The employee directory supports the full add/edit/deactivate workflow. Login is protected by account lockout and inactivity session expiry, and all data persists in browser storage with a demo reset control.
