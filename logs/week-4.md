# Week 4 — Feb 15-21, 2026

## Summary

Week 4 captures presentation prep work and a return to Surescripts certification testing. Surescripts responded that the failing issue was on their end and has now been resolved, so testing and debugging can continue.

## Entries

- 2026-02-16 | 4.0 hrs | Other
  - Activity: Collected data and worked on first draft slides.
  - Details: Used generated diagrams based on database schema and workflows.
  - Next: Add finishing touches (images, formatting) before submission.

- 2026-02-17 | 5.0 hrs | Testing & Debugging
  - Activity: Surescripts responded and confirmed the issue was on their end; it was resolved.
  - Next: Continue testing and debugging code.

- 2026-02-19 | 4.0 hrs | Coding
  - Activity: Implemented missing features for cancellation handling.
  - Details: Pharmacies can no longer deny a cancellation, cancellation messages are now received by the frontend, and fixed a backend-settings bug that broke passkey enrollment.

- 2026-02-20 | 1.5 hrs | Testing & Debugging
  - Activity: Fixed bug where renewal was blocked for Schedule II drugs.
  - Details: The logic and plan was solid, but our testing harness expected to us send a new prescription within that renewal     request, not just an approval, to test if we allow refills for scheduled drugs, which is illegal.

- 2026-02-20 | 2.5 hrs | Coding
  - Activity: Create dev-only option to bypass passkey for prescribing controlled substances to speed up coding/debugging.
  - Details: All fixes are now implemented.
  - Next: Rerun the tests to see if new patches broke previous code.

## Todo checklist

- [x] Follow up with Surescripts on failing certification issue
- [x] Confirm external staging issue resolution from Surescripts response
- [x] Resolve Schedule II renewal handling issue for certification test flow
- [x] Add dev-only passkey bypass for controlled-substance prescribing during debugging
- [~] Continue testing and debugging code after fix
- [ ] Rerun tests to verify new patches did not break previous code
- [ ] Complete testing (within 2-3 weeks)

Legend: [x]=done, [~]=in-progress, [ ]=not-started
