# Week 3 — Feb 9, 2026

## Summary

Week 3 captures initial work on Feb 9-14, 2026: communications with SureScript staging about failing test cases and a short team discussion to plan interim work while waiting for their response.

## Entries

- 2026-02-09 | 0.5 hrs | Other
  - Activity: Back-and-forth emailing SureScript staging about some issues on their end.
  - Note: Some test cases are unexpectedly failing; waiting for their response.
  - Description: Inbound messages to our EMR should automatcally pass if its inserted to our DB. The RxChangeRequest is also visible in the frontend but still fails. See [Screenshot from Surescript Certification Testing](../screenshots/surescripts/bug.png)

- 2026-02-09 | 1.5 hrs | Team Discussion
  - Activity: Describe issues faced with the testing harness and plan temporary mitigations while waiting on SureScript.
  - Outcome: Agreed on short-term plans: increase mocks/fixtures for local runs, capture failing test cases with reproduction steps, and prioritize highest-severity flows (EPCS and retraction).

- 2026-02-10 | 3.5 hrs | Research, Training, Learning
  - Activity: Research Redis to better understand caching system and applicability to our backend.
  - Note: Still awaiting instructions from SureScript staging on failing test cases, so I decided to learn Redis on my own to make productive progress. Redis can be used to reduce API calls and speed up loading times and app performance — considering trying it in a small personal project to get hands-on experience and improve user-facing performance.

- 2026-02-11 | 1.5 hrs | Team Discussion
  - Activity: Awaiting instructions/help from SureScripts; started planning how to work around issues on their end.
  - Outcome: Decided to wait before more testing to avoid redoing work once they locate the bug.


- 2026-02-11 | 1.5 hrs | Design
  - Activity: Designed updated RX inbox (`RxMessageView.tsx`) UI layout including status card, action island, denial reason workflow, and medication edit dialog to support renewal, change, and new prescription requests.
  - Note: Ensuring UI clearly communicates prescription state without overwhelming providers; validate layout decisions with real clinical workflows.

- 2026-02-11 | 5.0 hrs | Coding
  - Activity: Refactored component to support approve, deny, validate, and full medication edit workflows.
  - Reference: [See below: UI change description](#ui-change-examples-screenshots)

- 2026-02-12 | 3.0 hrs | Coding
  - Activity: Continued work from yesterday by adding local state updates, status mapping, SureScripts denial code handling, and UI action locking for renewal, change, and new prescription requests.
  - Outcome: Improved prescription workflow reliability and reduced dependency on page refreshes, making EMR inbox behavior more production-ready and aligned with backend state logic.

## Insights & implications

- Staging failures from SureScript can block progress; having local mocks/fixtures allows continued development.
- Prioritizing EPCS and retraction flows ensures security and compliance features are tested first.
- Team discussions help align on blockers and interim plans, reducing downtime.

## Actionable priorities (this week)

1. Finish capturing failing test cases and reproduction steps — High
2. Create local mocks/fixtures for SureScript interactions to enable local testing — High
3. Continue EMR EPCS/retraction implementation and add unit tests — Medium
4. Follow up with SureScript support and escalate if needed — Medium
5. Update team and supervisor on progress and any responses — Low

## Todo checklist

- [~] Investigate SureScript staging failures and follow up with support
- [x] Team discussion: issues with testing harness & interim plan
- [ ] Capture failing test cases with reproduction steps
- [ ] Create local mocks/fixtures for SureScript
- [ ] Add unit tests for EPCS/retraction flows
- [ ] Escalate to SureScript support if no response
- [x] Continue RX inbox workflow implementation in `RxMessageView.tsx` (approve/deny/edit/state transitions)
- [x] Add local state updates and status mapping to reduce page-refresh dependency
- [x] Implement SureScripts denial code mapping and denial-reason handling in UI
- [x] Add action locking for renewal, change, and new prescription request flows

Legend: [x]=done, [~]=in-progress, [ ]=not-started

## Short-term next steps

- Complete the failing case documentation and start building mocks.
- Run local tests with new fixtures to validate EPCS/retraction logic.
- Schedule a follow-up team sync if SureScript response is delayed.

## UI change examples (screenshots)

Reference folder: [screenshots/RxMessageView](../screenshots/RxMessageView/)

- Before: `screenshots/RxMessageView/Before.png`
  - The legacy RX message view used a generic request summary/details layout with simple right-rail actions.
  - Approve and deny were present, but the state transition and provider workflow context were less explicit in the main content area.

- After (Approve example): `screenshots/RxMessageView/Approve.png`
  - Added clearer prescription header/status presentation with an approved state badge.
  - Status card on the right confirms approval with timestamp, reducing ambiguity after action.
  - Action area supports approve/reject flow while preserving quick actions and clinical context.

- After (Deny example): `screenshots/RxMessageView/Deny.png`
  - Denied state is surfaced with a red status indicator and denial confirmation card.
  - Denial outcome is visible at a glance alongside the same order/timeline context used in approval.
  - Layout supports denial reason workflow and keeps action controls consistent with approval behavior.

## Owners & targets

- Primary developer: capture cases and build mocks (target: end of day)
- QA/Dev: add unit tests and run locally (target: tomorrow)
- Project lead: follow up with SureScript and update stakeholders (target: within 2 days)

## Notes & assumptions

- SureScript staging issues may be temporary; assume response within 24-48 hours. (has taken up to 4-5 days in the past though)
- Local mocks should mimic staging behavior closely to avoid false positives in testing.
- HIPAA compliance remains a priority; ensure any test data redacts PHI.
