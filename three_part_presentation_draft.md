# Benji Deliverable 5 Presentation Draft

Target length: 12-14 minutes total.

## Part 1 - Christopher Surette

Suggested time: 4-5 minutes

Topic: System background, component design, and backend/middleware connection

### Opening

Hi, my name is Christopher Surette. I am going to start by giving a quick overview of the Benji system and how our component design connects to the prototype we built for Deliverable 5.

Benji is an internal payroll management system designed for a local STEM education center. The center has instructors, tutors, supervisors, and payroll administrators who need a more reliable way to track employee hours, review timesheets, calculate payroll, and maintain payroll records.

The main problem Benji solves is that the current process depends on manual tracking, spreadsheets, and informal communication. That creates issues with payroll accuracy, approval accountability, and audit readiness.

### Component Design Overview

From our earlier deliverables, we organized Benji into seven main functional components:

1. Time Tracking
2. Approval Workflow
3. Payroll Calculation
4. Employee Records
5. Pay Stub and History
6. Reporting
7. Security and Access Control

For Deliverable 5, we focused the prototype on the most important complete workflow: an employee logs in, submits hours, an admin reviews the entry, and the system generates payroll output from approved time.

### Middleware and Architecture

Our planned architecture is a three-tier system:

1. A front-end presentation layer for the user interface.
2. A middleware and service layer for validation, business rules, and payroll logic.
3. A database layer for users, employees, time entries, pay stubs, and audit logs.

In the prototype, we simulated those layers in a browser-based version. The prototype uses local data instead of a full database, but it still demonstrates the same core behaviors:

- Login and role-based routing.
- Time-entry validation.
- Approval decision updates.
- Audit-style activity tracking.
- Payroll report calculations.

### Handoff

That gives us the technical structure behind the prototype. Next, Adrian will walk through the user journey map and explain how the screens support the main user workflow.

## Part 2 - Adrian Morton

Suggested time: 4-5 minutes

Topic: User Journey Map and prototype workflow

### Journey Map Overview

Hi, my name is Adrian Morton. I am going to explain the user journey map we created before building the prototype.

The goal of the journey map was to make sure the prototype followed a real payroll workflow instead of just showing separate screens. We identified the main users as employees, program supervisors, payroll administrators, and the CEO as an executive stakeholder.

The primary journey we implemented starts with an employee and ends with an administrator generating payroll information.

### Implemented Phases

The implemented phases are:

1. Access system
2. Employee dashboard
3. Submit hours
4. View timesheet status
5. Admin review queue
6. Admin review decision
7. Payroll report generation

In the first phase, the user logs in. The system checks the user's role and sends employees to the employee dashboard and administrators to the admin dashboard.

On the employee side, the user can view a summary of the current pay period, open the Log Hours screen, and submit a time entry with a date, hours worked, program or role, and notes.

The system validates the entry before saving it. For example, it checks that the date is not in the future, that the hours are within a valid range, and that the entry is not a duplicate.

After submission, the employee can go to My Timesheets and see the entry status. At first, the status is pending.

On the admin side, the administrator opens the Review Queue, selects the employee's submitted entry, reviews the details, and chooses to approve, reject, or flag it. The prototype then updates the entry status and records the decision.

Finally, the administrator can open the Reports screen and generate a payroll report based on approved entries.

### Screens and Components

The main screens supporting this workflow are:

- SCR-01 Login
- SCR-02 Employee Dashboard
- SCR-04 Time Entry Form
- SCR-05 My Timesheets
- SCR-03 Admin Dashboard
- SCR-06 Approval Queue
- SCR-07 Timesheet Review
- SCR-12 Payroll Report Generator

Each screen maps back to one or more of our functional components, especially Time Tracking, Approval Workflow, Payroll Calculation, Reporting, and Security.

### Handoff

Now that the journey and screens are covered, Roger will demonstrate the prototype and summarize the testing results.

## Part 3 - Roger Mendez

Suggested time: 4-5 minutes

Topic: Prototype demonstration and functional testing results

### Prototype Demo Introduction

Hi, my name is Roger Mendez. I am going to demonstrate the working prototype and then summarize the functional testing results.

The prototype is opened from the `prototype/index.html` file. It is a browser-based version of Benji that demonstrates the core Deliverable 5 workflow.

### Demo Steps

First, I log in as the employee, Emma Rivera.

After logging in, the employee dashboard shows the current pay-period summary, pending entries, approved hours, and recent activity.

Next, I open the Log Hours screen. Here the employee enters the work date, hours worked, program or role, and optional notes. When I submit the entry, the system validates it and saves it as a pending timesheet entry.

Then I open My Timesheets and show that the new entry is visible with a pending status.

Next, I log out and switch to the admin account.

On the admin dashboard, the administrator can see pending approvals, active employees, approved entries, and audit events. I open the Review Queue, select the employee's pending timesheet, review the details, and approve it.

After the approval is saved, the system updates the timesheet status and records the action.

Finally, I open the Reports screen and generate a payroll report. The report shows approved hours, gross pay, deductions, net pay, and totals.

### Functional Testing

For functional testing, we prepared more than the required minimum of ten test cases. The final test set covers:

- Valid and invalid login.
- Role-based dashboard routing.
- Valid time-entry submission.
- Future-date validation.
- Invalid hour validation.
- Duplicate-entry prevention.
- Approval queue display.
- Approving a timesheet entry.
- Rejecting or flagging entries with required notes.
- Employee visibility of reviewed status.
- Payroll report generation.

All listed test cases passed for the prototype.

### Closing

Overall, Deliverable 5 shows that Benji's requirements, screen design, and component design can support a complete payroll workflow. The prototype demonstrates the main user journey from login through payroll reporting, and the functional testing confirms the key interactions and validation rules.

