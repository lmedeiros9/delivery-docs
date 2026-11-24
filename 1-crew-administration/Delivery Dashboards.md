# Delivery Dashboards Playbook

Nov 23, 2026 · @Lindsay Medeiros

## Overview

Three Salesforce dashboards answer the core delivery questions: are our people loaded right, are clients getting what they pay for, and is the work moving with quality. All three run as Lindsay Medeiros and refresh on open (click Refresh for live numbers). They currently sit in Lindsay's Private Dashboards folder and move to a shared Delivery folder once an admin creates it.

| Dashboard | Question it answers | Primary audience | Link |
| --- | --- | --- | --- |
| Delivery – People v2 | Is the crew on goal, what's planned, do we have capacity to hire? | Director of Delivery, leadership | [Open](https://clientcloudcare.lightning.force.com/lightning/r/Dashboard/01ZhR000007XPmnUAG/view) |
| Delivery – Clients v2 | Are clients using their contracted hours, who is over, what renews, how happy are they? | Director of Delivery, leadership, client leads | [Open](https://clientcloudcare.lightning.force.com/lightning/r/Dashboard/01ZhR000007XQ7lUAG/view) |
| Delivery – Work | What is waiting, is maker-checker happening, who is completing work, is the data clean? | Director of Delivery, crew leads | [Open](https://clientcloudcare.lightning.force.com/lightning/r/Dashboard/01ZhR000007XVIjUAO/view) |

**Suggested rhythm**

- **Weekly (crew meeting):** Work dashboard — past due, stalled, missed checks, data quality by person. Each person leaves with their own fix-it list.
- **Mid-month:** People (pace vs goal) and Clients (hours used vs % of month elapsed) to catch over- and under-delivery while there is still time to act.
- **Monthly (leadership):** headline rows of all three, plus open capacity (hiring), created vs completed, renewals and CSAT.

## Delivery – People v2

Answers: is each crew member on pace for their utilization goal, how much work is planned for the next three months, and where do we have room — or a need — to hire.

**Scope:** active billable crew. Courtney Schmidt, Wendy DeCesare, Nicole DeMartine and Mary Crozier are excluded (they don't bill clients). "Cloudcare Admin" is treated as unassigned work, not a person.

| Component | What it shows | How to read it |
| --- | --- | --- |
| Crew Pace vs Utilization Goal | Billable hours ÷ goal hours to date | 100% = exactly on goal. Red < 80%, amber 80–95%, green ≥ 95%. |
| Crew Billable Hours | Client hours logged this month | Raw volume; compare with goal hours to date. |
| Goal Hours to Date | Capacity × goal %, prorated to today | The target the crew should have hit by today. |
| Unassigned Planned Hours | Planned hours on Cloudcare Admin, this month + next 2 | Work sold but not staffed — assign it or it eats capacity. |
| Actual Billable vs Goal to Date | Per person, actual vs prorated goal | Gaps show who is behind or ahead this month. |
| Planned Hours as % of Goal | Per person, this month and next 2 | Over 100% = planned beyond goal (burnout risk); low = open capacity. |
| Open Capacity vs Goal (Hiring View) | Goal hours minus planned hours, stacked by person per month | Below zero = over-planned. Consistently small or negative totals = case for hiring. |
| Capacity, Goal & 90-Day Avg Hours | Per person: capacity, goal hours, rolling 90-day average hours | 90-day average includes internal work; shows sustained load. |
| Actual Client Hours by Person | Client hours by work date, last 6 months | Trend of who is delivering client work. |

**Baseline (23 Nov 2026):** crew at 92% of goal pace; 394 billable hours vs 429 goal to date; 146.5 unassigned planned hours over three months. Nicole Hall is planned at 133–137% of goal and Lauren Greeno at 117% in December, while most others have open capacity in Dec–Jan.

## Delivery – Clients v2

Answers: are Managed Service clients using the hours they pay for, who is over budget, whose block hours or contract is running out, and how satisfied they are.

**Scope:** active client projects; internal Cloudcare projects excluded. Hours are counted by the date the work happened, not the date it was entered.

| Component | What it shows | How to read it |
| --- | --- | --- |
| MS Contracted Hours | Total monthly hours across Managed Service + Client Management contracts | Monthly capacity we've sold. |
| MS Hours Used | % of contracted hours used so far this month | Compare with Month Elapsed next to it. |
| Month Elapsed | % of the calendar month gone | Used well ahead of elapsed = overage risk; well behind = under-delivery or churn risk. |
| Clients Over Hours | Count of projects with negative monthly or block hours remaining | Green 0, amber 1–2, red 3+. |
| Renewals ≤ 90 Days | Projects expiring within 90 days, including expired-but-active | Start renewal or close-out conversations. |
| Avg CSAT | Average latest CSAT score, active-contract clients | Red < 4, amber 4–4.5, green ≥ 4.5. |
| MS Hours Used vs Contracted | Per client, contracted vs used this month | Spot clients near or over their monthly hours. |
| Client Hours Delivered by Month | Last 12 months, stacked by contract type | Delivery volume trend. |
| Block Hours Remaining | Ongoing Support & Project contracts, lowest first | Low balances need a reload or a client conversation. |
| CSAT by Client | Latest score per client, lowest first | Who to check in with. |
| Clients Over Hours (table) | Monthly and block hours remaining for over-budget projects | Negative = hours over. |
| Renewals & Expirations ≤ 90 Days | Days left per project | Negative = already expired. |
| CSAT Surveys Overdue | Active clients never surveyed or > 180 days since survey | 0 days = never surveyed. |

**Baseline (23 Nov 2026):** 506 contracted MS hours/month, 79% used at 77% of month elapsed. ILAO, Hutchcraft, Casa Familiar and NextOp were above 90% used. 5 projects over hours (Russian Riverkeeper −60.5 monthly, Landmark −34.8 block). 5 renewals within 90 days; UT Health expired 10 Nov but is still active. Average CSAT 4.78 across 9 scored clients; 18 active clients overdue for a survey.

## Delivery – Work

Answers: what work is waiting or stuck, whether maker-checker review is happening, who is completing work, whether we keep up with incoming work, and how complete the project line data is.

**Scope:** project lines on active client projects. Excluded: internal Cloudcare projects, default time lines, and "Ongoing" bucket lines (meetings, PM, invoicing). Completion dates come from status history.

**Headline row:** Open Work Items · Past Due · Stalled · In Internal Review · Checks Missed (30 days) · Done ≤ 30 Days (6 months).

| Section | Component | How to read it |
| --- | --- | --- |
| Waiting | Open Work by Status | Where work piles up; stacked by priority ("-" = no priority set). |
| Waiting | Longest in Current Status | Lines sitting longest since their last status change. Open the report for each line's status. |
| Waiting | Past Due by Person | Open lines past their planned end date. |
| Waiting | Stalled by Person | In Progress / Internal Review lines with no hours logged in 14+ days. |
| Maker-checker | Missed Checks by Assignee | Checker-required lines completed in 30 days with no checker and no waiver. Target: zero. |
| Maker-checker | Required Work by Checker | Who is doing reviews; "-" = no checker (waived or missed). |
| Maker-checker | Sent Back from Review | Lines moved out of Internal Review backwards — a rework signal. |
| Throughput | Completed by Person | Lines moved to Completed per month, by assignee. |
| Throughput | Work in Hand by Person | Active lines per person by status; spots overload. |
| Trend | New Work Created | Lines created per month; compare with completed to see if backlog grows. |
| Trend | Avg Days to Complete | Created → Completed, by completion month. Long-running lines pull it up; read with Done ≤ 30 Days. |
| Data quality | % Complete by Person | Share of 5 core fields filled: Environment, Due Date, Allotted hours, Priority, C2 Team. |
| Data quality | No Internal Docs | Lines with no internal documentation links. |
| Data quality | No Sub-Tasks | Lines with no sub-tasks. |

Follow-up reports not on the dashboard: **DBv2W\_Missing Fields Detail** (per-line fix-it list), **DBv2W\_Unowned or Inactive Owner**, **DBv2W\_Checker Required - Not Covered** (full list).

**Baseline (23 Nov 2026):** 245 open items, 31 past due (11 for Jane Stilling), 42 stalled. Of 31 checker-required lines completed in 30 days, 22 (71%) had no checker or waiver; none of the 7 lines in Internal Review has a checker assigned. 38% of lines complete within 30 days; average 155 days. Lines past Backlog are 58% complete on core fields (Lauren Greeno 86%, Jane Stilling and Jalisha Sumler 44%); 119 lack internal docs and 89 lack sub-tasks.

## Definitions and business rules

| Term | Definition | Source in Salesforce |
| --- | --- | --- |
| Utilization goal | Chris Oliver 25%, Lindsay Medeiros 60%, all other crew 90% of monthly capacity | Hardcoded in report formulas (no field) |
| Goal hours | Capacity/month × utilization goal | Resource: Capacity/month |
| Goal hours to date | Goal hours × (day of month ÷ days in month) | Calendar days, not working days |
| Billable hours | Hours logged to non-Cloudcare clients this month | Resource: Billable Hours this Month |
| Planned hours | Monthly planned effort on allocations | Project Allocation: Monthly Planned Effort |
| Unassigned work | Planned hours allocated to the "Cloudcare Admin" placeholder | Project Allocation |
| Hours used (MS) | Monthly Hours − Monthly Hours Remaining | Project |
| Over hours | Monthly or block (Project) hours remaining below zero | Project |
| CSAT | Latest CSAT score and last survey date | Project: Client |
| Done | Status = Completed; completion date taken from status history | Project Line + history |
| Stalled | In Progress or Internal Review, no hours logged in 14+ days | Project Line: Last Actuals Update |
| Past due | Open, planned end date before today | Project Line: Planned End |
| Covered (maker-checker) | Checker assigned, or a waiver reason entered | Project Line: Checker, Waiver Reason |
| Sent back | Status moved from Internal Review to anything other than UAT/Delivery or Completed | Status history |
| Completeness | Applies once a line leaves Backlog; 5 core fields plus internal docs and sub-tasks | Project Line |

## Known limitations

These are constraints of current fields and access, not errors. Read the affected numbers with them in mind.

- **Open capacity can be understated.** A person with no allocation in a month doesn't appear in that month's hiring view.
- **Goal pacing uses calendar days.** Expect slightly harsh readings early in the month and on Mondays.
- **Former staff appear in history.** 6- and 12-month hours charts include people who have left, so history stays complete.
- **Time in stage is approximate.** "Longest in Current Status" measures from the last status change; lines never changed since creation don't appear.
- **Review turnaround and rejections aren't reportable.** Approval records can't be reported on; "Sent Back from Review" is the closest proxy.
- **Estimate vs actual hours isn't available.** Project line effort fields don't hold lifetime logged hours, and current access can't join time entries to line estimates.
- **Two "Not Started" values look identical.** The picklist has Not\_Started and "Not Started"; reports show both as "Not Started".
- **Data quality limits other views.** Due dates, priority and C2 Team are often blank, so past-due and priority views undercount until the fields are filled consistently.

## Maintenance

**Where things live.** Reports are in Lindsay's private reports folder: "DBv2\_" prefix for People and Clients, "DBv2W\_" for Work. The original "Delivery – People" and "Delivery – Clients" dashboards are untouched and can be retired once v2 is adopted. Build scripts live in the C2HQ Prod project under scripts/dashboards; rerunning them rebuilds every report and dashboard from one definition.

**Common changes**

| Change | Where |
| --- | --- |
| Utilization goal changes, or someone joins/leaves | Goal CASE formula in the People reports (scripts: reports.py, goal function) |
| Exclude or include a person from People views | Exclusion list in the People reports (scripts: sfapi.py, EXCLUDE) |
| Change stall threshold (14 days) or survey window (180 days) | The matching report filter |
| Change what counts as complete | Missing Fields formula in the Completeness reports |

**Open items**

- [ ] Ask admin for a shared "Delivery" dashboard folder with view access for leadership; move all three dashboards there.
- [ ] Ask admin to merge the duplicate "Not Started" status values.
- [ ] Optional, when fields are allowed: a utilization-goal field on Resource, "has internal docs" / "has sub-tasks" checkboxes, and status-change date stamps.
- [ ] Optional, access: read on project line fields in time-entry report types, to enable estimate vs actual.
- [ ] Retire the original dashboards and their reports after v2 adoption.
