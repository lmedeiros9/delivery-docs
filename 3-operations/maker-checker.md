---
title: Maker-Checker
parent: "3 | Operations"
nav_order: 3
---

# Maker-Checker

- **Purpose:** Explain how every piece of work gets built, reviewed, and delivered.
- **Owner:** Director of Delivery
- **Last reviewed:** 2026-11-12
- **Applies to:** Everyone on the delivery crew

Maker-Checker is our case lifecycle. The builder (the maker) stays attached to their work, and a second person (the checker) verifies quality before anything reaches the client.

## The five quality pillars

Every deliverable is measured against these five pillars. Together they define "done."

| Pillar | What it means | Examples |
|--------|---------------|----------|
| **Security** | Data integrity, compliance, access controls, audit trail | Proper field permissions, no hardcoded values, change tracking |
| **Scalability** | Performance, platform limits, future-proofing | Handles growth, stays within governor limits, efficient queries |
| **Supportability** | Documentation, maintainability, admin handoff readiness | Flow diagrams, clear comments, a runbook for the support team |
| **Standardized Logic** | Follows C2 patterns, clean and reusable | Standard naming, reuses existing flows and components |
| **Seamless UX** | End-user experience, adoption readiness, training | Intuitive screens, training materials ready, user buy-in planned |

## How work moves

| Status | What happens | Who |
|--------|--------------|-----|
| **New** | A support request arrives and goes to the Client Lead. | Client Lead |
| **Ready to Assign** | Triage is done. The request lands in the Ready for Takeoff queue and the crew gets a Slack alert. | Client Lead |
| **In Progress** | A crew member claims the work by assigning themselves, then builds it. The maker stays on the record through close. | Maker |
| **Ready for Check** | The maker hands off for review. The request lands in the Ready for Check queue and the crew gets a Slack alert. | Maker |
| **Check Complete** or **Revisions Required** | A checker claims it, runs the Start Audit flow, and verifies the five pillars. | Checker |
| **Ready to Deliver** | Approved work waits while the Client Lead prepares delivery. | Client Lead |
| **Closed** | Final delivery to the client. The maker and checker stay on the record for reporting. | Client Lead |

## The audit

The checker runs a guided flow with four steps:

1. Review a summary of the maker's work.
2. Verify each of the five pillars. All five must pass to approve.
3. Record the review: a reason and notes if revisions are needed, or optional positive feedback if approved.
4. Decide: **Approved** or **Revisions Required**.

If revisions are required, the request stays in the Ready for Check queue with the checker's notes. The maker fixes it, and the work gets audited again.

## When an audit isn't needed

Low-risk work can skip review. Mark **Checker Not Required** and the request goes straight to Ready to Deliver. Skipped review does not mean skipped standards. The work still needs clear documentation and has to follow C2 standards.

> Still being defined: exactly which types of work qualify for a skipped review.
{: .note }

## If something goes wrong

A checker who finds a blocker, hits a split decision, or sees a timeline risk should follow [Escalation Paths]({{ site.baseurl }}/6-communications/escalation-paths.html).

## What we measure

Audit results feed reporting on first-pass approval rate, audit cycle time, which pillars fail most often, and consistency across checkers. The goal is to improve the process, so use these numbers to find patterns.

[Open the full Maker-Checker specification](PASTE-LINK-TO-MAKER-CHECKER-SPEC)
