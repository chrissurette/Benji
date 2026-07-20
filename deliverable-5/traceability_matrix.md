# Benji Traceability Matrix


## Journey Phase → Screen → Test Case

| # | Journey Phase | User Action | Prototype Screen | Test Case(s) | Status |
|---|---|---|---|---|---|
| 1 | Access system | User enters credentials; system routes by role | SCR-01 Login | TC-01, TC-02, TC-03 | Pass |
| 2 | Employee dashboard | Employee reviews pay-period status | SCR-02 Employee Dashboard | Supported by TC-01 (post-login landing) | Pass |
| 3 | Submit hours | Employee enters date, hours, program, notes | SCR-04 Time Entry Form | TC-04, TC-05, TC-06, TC-07 | Pass |
| 4 | View status | Employee checks own entries and review outcome | SCR-05 My Timesheets | TC-11 | Pass |
| 5 | Review queue | Admin opens submitted entries | SCR-06 Timesheet Approval Queue | TC-08 | Pass |
| 6 | Record decision | Admin approves, rejects, or flags entry | SCR-07 Timesheet Review | TC-09, TC-10 | Pass |
| 7 | Payroll report | Admin generates payroll output | SCR-12 Payroll Report Generator | TC-12 | Pass |

## Test Case Coverage Summary

| Test Case | Verifies | Journey Phase | Screen |
|---|---|---|---|
| TC-01 | Valid employee login and dashboard routing | Access system | SCR-01 → SCR-02 |
| TC-02 | Invalid credentials rejected | Access system | SCR-01 |
| TC-03 | Role-based routing to Admin Dashboard | Access system | SCR-01 → SCR-03 |
| TC-04 | Valid time entry saved as PENDING | Submit hours | SCR-04 |
| TC-05 | Future-dated entry rejected | Submit hours | SCR-04 |
| TC-06 | Invalid hours rejected | Submit hours | SCR-04 |
| TC-07 | Duplicate entry rejected | Submit hours | SCR-04 |
| TC-08 | Pending entries appear in review queue | Review queue | SCR-06 |
| TC-09 | Approve entry; audit event recorded | Record decision | SCR-07 |
| TC-10 | Reviewer notes required to reject/flag | Record decision | SCR-07 |
| TC-11 | Employee sees updated review outcome | View status | SCR-05 |
| TC-12 | Payroll report with gross/deductions/net/totals | Payroll report | SCR-12 |

## Coverage Notes

- All 7 implemented journey phases have at least one supporting prototype screen.
- 6 of 7 phases have direct functional test coverage; the Employee Dashboard (phase 2) is exercised indirectly as the post-login landing verified by TC-01.
- Supporting screens SCR-03 (Admin Dashboard), SCR-08 (Employee Directory), and SCR-10 (Pay Stub History) are implemented with demo data and are reached during the core journey.
- All 12 functional test cases map to a journey phase, confirming the prototype reflects the end-to-end workflow rather than isolated features.
