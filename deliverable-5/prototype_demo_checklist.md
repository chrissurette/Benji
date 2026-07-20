# Prototype Demo Checklist

Use this checklist while recording the Deliverable 5 presentation.

## Before Recording

- Open `deliverable-5/prototype/index.html` in Chrome or Edge.
- Keep the final Word document available for the journey-map overview.
- Keep `functional_test_cases.csv` available for the testing-results section.

## Demo Steps

1. Show the Benji login screen.
2. Log in as the employee account: `emma.employee@benji.test`.
3. Open the Employee Dashboard and point out the pay-period summary.
4. Go to Log Hours and submit a valid time entry.
5. Show My Timesheets and confirm the entry is pending.
6. Log out and use the admin account: `admin.payroll@benji.test`.
7. Open the Admin Dashboard and Review Queue.
8. Review the employee's pending entry.
9. Approve the entry and point out the saved decision message.
10. Open Reports and generate the payroll report.
11. Show gross pay, deductions, net pay, and totals.
12. Log back in as the employee and confirm the entry status changed to approved.

## Closing Points

- The prototype demonstrates one complete user journey from login to payroll output.
- The test cases cover authentication, time submission, validation, approval, status visibility, and reporting.
- The production system would replace simulated in-memory data with the planned Spring Boot and PostgreSQL backend.
