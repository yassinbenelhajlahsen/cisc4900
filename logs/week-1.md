# Week 1 — Jan 25–31, 2026

## Summary

This Week 1 document consolidates work from Jan 25–31, 2026. It contains a short daily log, a prioritized set of steps and plans for the coming sprint, and a tracked todo list derived from the raw entries.

Key focus areas:

- Documentation: README for testing prescription send/receive flows.
- Testing & Debugging: Test and debug interactions with Surescript Staging; add Pytest cases and fixtures.
- Non-technical: Resume updates, supervisor coordination, and HIPAA compliance planning.

## Raw entries (source)

- 1/25/26 | 2.0 hrs | Other
  - Activity: Created new resume based on experience, project skills and education.
  - Note: Finding a good format and resume editor website.

- 1/26/26 | 1.0 hr | Supervisor Discussion
  - Activity: Discuss with supervisor about CISC 4900 requirements and plan how to communicate project needs and make sure we don't break NDA.

- 1/28/26 | 1.0 hr | Other
  - Activity: Updated resume and added keywords and metrics.
  - Note: Many jobs look for specific keywords to match; metrics show impact.

- 1/28/26 | 1.5 hrs | Documentation
  - Activity: Create `README.md` for plan to test prescription sending/receiving.
  - Note: Start QA/testing soon before app launch.

- 1/29/26 | 3.5 hrs | Testing & Debugging
  - Activity: Test and debug code against Surescript Staging.
  - Note: Finish testing and find more edge cases.

- 1/30/26 | 6.0 hrs | Testing & Debugging
  - Activity: Continue to test and debug code.
  - Note: Run more tests using Pytest before pushing code to main to speed up QA.

- 1/31/26 | 0.5 hrs | Team Discussion
  - Activity: Plans for next week.
  - Note: Continue working on prescription debugging to ensure HIPAA compliance.

## Steps & Plans (actionable)

1. Finish Surescript Staging test pass
   - Owner: Primary developer
   - Why: Identify and document all failing cases and reproduction steps so tests can be added.
   - Success criteria: All previously failing cases either pass or have tracked issues with a clear reproduction and mitigation plan.

2. Add Pytest cases and fixtures
   - Owner: Primary developer
   - Why: Prevent regressions and speed up QA by running automated tests locally and in CI.
   - Plan: Add tests for the reproduction steps from staging; create fixtures or mocks for Surescript where possible.

3. Finalize README test instructions
   - Owner: Developer/Documentation
   - Why: Make it straightforward for other contributors to run tests and avoid committing secrets.
   - Include: How to set environment variables, run Pytest, and point to staging (securely).

4. Resume improvements
   - Owner: You
   - Why: Resume is updated; add metric-driven bullets from the sprint (e.g., tests added, bugs reduced, throughput impacts).

5. HIPAA compliance checklist
   - Owner: Team / Project lead
   - Why: Ensure debugging and logs do not expose PHI; maintain compliance for e-prescribing flows.
   - Deliverable: Short checklist with logging rules, test-data redaction, and access controls.

## Todo list (actionable items)

- [x] Create new resume (1/25/26) — master resume created; pick an editor/format and keep canonical copy.
- [x] Supervisor discussion: CISC 4900 & NDA (1/26/26) — aligned on requirements and NDA constraints.
- [x] Update resume with keywords & metrics (1/28/26) — added keywords/metrics; retain a metrics list for future updates.
- [x] Create `README.md` for testing prescription sending/receiving (1/28/26) — initial README created; expand with run steps.
- [~] Test & debug against Surescript Staging (1/29/26) — in progress; capture failing cases and reproduction steps.
- [~] Add Pytest tests & fixtures; run locally before merging (1/30/26) — in progress; add fixtures/mocks to speed local runs.
- [ ] Prepare HIPAA compliance checklist (1/31/26) — draft checklist to be produced and reviewed.
- [x] Team discussion: plans for next week (1/31/26) — short planning meeting held; next actions assigned.

Legend: [x]=done, [~]=in-progress, [ ]=not started

## Short-term next steps (this week)

- Complete the staging test pass and list all edge cases.
- Convert staging edge cases into Pytest tests (start with the highest-severity failures).
- Add env var guidance and `.env.template` to README; do NOT commit secret values.
- Draft HIPAA checklist and schedule a short follow-up meeting to review.

## Notes & assumptions

- Staging credentials must be shared securely; do not commit secrets.
- Pytest is the test framework in use; if the project uses another runner, adapt accordingly.

## How to use this file

- Use this as the canonical Week 1 plan. Update the checkboxed todo list as tasks progress and add single-line notes for completed items with a date and name.

---

_Generated from daily entries for Jan 25–31, 2026._
