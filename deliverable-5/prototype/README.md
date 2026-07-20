# Benji Payroll Prototype

Open `index.html` in a browser to run the prototype.

## Demo Accounts

| Role | Email | Password |
|---|---|---|
| Employee | emma.employee@benji.test | Employee#123 |
| Admin | admin.payroll@benji.test | Admin#123 |

## Recommended Demo Flow

1. Log in as Emma Rivera using the employee account.
2. Open **Log Hours**, submit a time entry for `2026-07-19`.
3. Confirm the app redirects to **My Timesheets** and shows the new entry as `PENDING`.
4. Log out and use the admin login.
5. Open **Review Queue**, review Emma's pending entry, and approve it.
6. Open **Reports** and generate the payroll report.
7. Log out, log back in as Emma, and confirm the timesheet entry now shows `APPROVED`.

## Prototype Scope

This is a browser-based prototype of the Benji workflow described in Deliverables 1-4. It uses in-memory JavaScript data to simulate the planned middleware and database behavior. Implemented screens include:

- SCR-01 Login
- SCR-02 Employee Dashboard
- SCR-03 Admin Dashboard
- SCR-04 Time Entry Form
- SCR-05 My Timesheets
- SCR-06 Timesheet Approval Queue
- SCR-07 Timesheet Review
- SCR-08 Employee Directory
- SCR-10 Pay Stub History
- SCR-12 Payroll Report Generator

