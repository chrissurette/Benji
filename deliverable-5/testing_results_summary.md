# Functional Testing Results Summary

The Deliverable 5 prototype was tested against the functional test cases in `functional_test_cases.csv`.

## Test Coverage

| Area | Covered Test Cases |
|---|---|
| Login and authentication routing | TC-01, TC-02, TC-03 |
| Employee time entry submission | TC-04 |
| Time-entry validation | TC-05, TC-06, TC-07 |
| Admin approval workflow | TC-08, TC-09, TC-10 |
| Employee review visibility | TC-11 |
| Payroll reporting | TC-12 |
| Security hardening (lockout, session timeout) | TC-13, TC-14 |
| Persistence and demo reset | TC-15, TC-16 |
| Report export | TC-17 |
| Pay stub generation | TC-18 |
| Employee management | TC-19, TC-20 |

## Results

| Metric | Result |
|---|---|
| Total functional tests | 20 |
| Passed | 20 |
| Failed | 0 |
| Blocked | 0 |
| Overall status | Pass |

## Notes

- The prototype validates future dates, invalid hour ranges, duplicate time entries, and inactive employee records.
- Admin decisions update the time-entry state and record an audit event; state now persists in browser localStorage across reloads, with a Reset Demo Data control to restore the seeded scenario.
- Payroll reporting calculates gross pay, deductions, net pay, and totals for approved entries, and supports CSV download and print/save-as-PDF output.
- Finalizing a pay run generates pay stubs per employee from approved entries and guards against paying the same entry twice.
- Login is protected by a five-attempt account lockout (15 minutes) and sessions expire after 15 minutes of inactivity.
- Remaining production gaps are real database persistence, JWT/BCrypt-backed authentication, and server-generated PDF export; these require the planned Spring Boot/PostgreSQL backend.
