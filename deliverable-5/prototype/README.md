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
7. Use **Export CSV** or **Print / Save PDF** to export the report, then click **Finalize Pay Run** to generate pay stubs.
8. Open **Employees** to add, edit, or deactivate an employee record.
9. Log out, log back in as Emma, and confirm the timesheet entry shows `APPROVED` and the new stub appears under **Pay Stubs**.
10. Use **Reset Demo Data** on the login screen to restore the seeded scenario before re-recording a demo.

## Prototype Scope

This is a browser-based prototype of the Benji workflow described in Deliverables 1-4. It simulates the planned middleware and database behavior with JavaScript service functions and browser localStorage persistence (all data survives reloads; use **Reset Demo Data** to restore the seed scenario). Implemented screens include:

- SCR-01 Login
- SCR-02 Employee Dashboard
- SCR-03 Admin Dashboard
- SCR-04 Time Entry Form
- SCR-05 My Timesheets
- SCR-06 Timesheet Approval Queue
- SCR-07 Timesheet Review
- SCR-08 Employee Directory (with add/edit/deactivate workflow)
- SCR-10 Pay Stub History (fed by pay-run finalization)
- SCR-12 Payroll Report Generator (with CSV export, print, and pay-run finalization)

## Security Behavior

- Five failed login attempts lock the account for 15 minutes.
- Sessions expire after 15 minutes of inactivity and return the user to the login screen.
- Deactivated employees cannot submit new time entries.

