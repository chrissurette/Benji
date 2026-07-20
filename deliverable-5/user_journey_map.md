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

## Prototype Coverage

The prototype implements the complete core journey from employee login through payroll report generation. Pay-stub history and employee directory are included as supporting screens with static demo data.
