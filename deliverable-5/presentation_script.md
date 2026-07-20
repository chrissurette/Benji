# Benji Deliverable 5 Presentation Script

Target length: 13-14 minutes.

## Adrian Morton - Component Design and Journey Map (about 4 minutes)

Introduce Benji as an internal payroll management system for a STEM education center. Explain that Deliverable 5 converts the previous requirements and component design into a prototype and functional testing plan.

Cover the main stakeholders: instructors/tutors, program supervisors, payroll administrators, the CEO, and the development/QA team.

Walk through the user journey map:

1. User logs in.
2. Employee views dashboard.
3. Employee submits hours.
4. Employee checks timesheet status.
5. Admin reviews the approval queue.
6. Admin approves, rejects, or flags the entry.
7. Admin generates payroll report.
8. Employee can view pay history.

Point out that the prototype implements the core journey from login through report generation.

## Christopher Surette - Middleware, Logic, and Testing Approach (about 4 minutes)

Explain the planned architecture from the previous deliverables: React/TypeScript front end, Spring Boot service layer, and PostgreSQL database.

Explain how the prototype simulates those layers:

- Login and role routing simulate security middleware.
- Time entry checks simulate validation middleware.
- JavaScript service functions simulate business logic.
- In-memory arrays simulate database tables.
- Audit entries simulate audit logging.

Summarize the implemented components:

- FC-01 Time Tracking
- FC-02 Approval Workflow
- FC-03 Payroll Calculation
- FC-06 Reporting
- FC-07 Security and Access Control

Explain the test strategy. The team prepared 12 functional tests covering login, role routing, valid submission, validation failures, approval behavior, employee status visibility, and payroll report generation.

## Roger Mendez - Prototype Demo and Results (about 5-6 minutes)

Open `prototype/index.html`.

Demo flow:

1. Log in as `emma.employee@benji.test` with `Employee#123`.
2. Open Log Hours.
3. Submit a valid time entry.
4. Show My Timesheets and confirm the entry is pending.
5. Log out.
6. Use Admin Login.
7. Open Review Queue.
8. Review Emma's pending entry.
9. Approve the entry.
10. Open Reports and click Generate Report.
11. Show gross pay, deductions, net pay, and totals.
12. Optionally log back in as Emma and show the approved status.

Close by summarizing testing results: all 12 planned functional tests are marked pass in the report. Mention remaining prototype limitations: no real database persistence, no production JWT/session handling, and no real PDF/CSV export yet.

## Closing

Benji's Deliverable 5 shows that the earlier requirements and component design can support a complete payroll workflow. The prototype demonstrates the main user journey and the functional tests verify the most important interactions before full implementation.
