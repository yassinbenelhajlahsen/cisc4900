# Week 3 — Feb 9, 2026

## Summary

Week 3 captures initial work on Feb 9-14, 2026: communications with SureScript staging about failing test cases and a short team discussion to plan interim work while waiting for their response.

## Entries

- 2026-02-09 | 0.5 hrs | Other
  - Activity: Back-and-forth emailing SureScript staging about some issues on their end.
  - Note: Some test cases are unexpectedly failing; waiting for their response.

- 2026-02-09 | 1.5 hrs | Team Discussion
  - Activity: Describe issues faced with the testing harness and plan temporary mitigations while waiting on SureScript.
  - Outcome: Agreed on short-term plans: increase mocks/fixtures for local runs, capture failing test cases with reproduction steps, and prioritize highest-severity flows (EPCS and retraction).

- 2026-02-10 | 3.5 hrs | Research, Training, Learning
  - Activity: Research Redis to better understand caching system and applicability to our backend.
  - Note: Still awaiting instructions from SureScript staging on failing test cases, so I decided to learn Redis on my own to make productive progress. Redis can be used to reduce API calls and speed up loading times and app performance — considering trying it in a small personal project to get hands-on experience and improve user-facing performance.

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

Legend: [x]=done, [~]=in-progress, [ ]=not-started

## Short-term next steps

- Complete the failing case documentation and start building mocks.
- Run local tests with new fixtures to validate EPCS/retraction logic.
- Schedule a follow-up team sync if SureScript response is delayed.

## Owners & targets

- Primary developer: capture cases and build mocks (target: end of day)
- QA/Dev: add unit tests and run locally (target: tomorrow)
- Project lead: follow up with SureScript and update stakeholders (target: within 2 days)

## Notes & assumptions

- SureScript staging issues may be temporary; assume response within 24-48 hours. (Has taken up to 4-5 days in the past though)
- Local mocks should mimic staging behavior closely to avoid false positives in testing.
- HIPAA compliance remains a priority; ensure any test data redacts PHI.
