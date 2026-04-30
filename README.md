# privacy-policy

Public policy source for Welders Helper suite store and in-app privacy disclosures.

This repo is the canonical public policy/static-page repo for shared Welders Helper language plus per-app overlays. Keep app behavior truth in the app repo, but keep public privacy, terms, account-deletion, and store-disclosure pages here so Apple/Google release work does not drift across apps.

Commit and push coherent GitHub checkpoints after policy wording, app page, store-disclosure, or release-checklist changes so every machine sees the same public policy truth.

## Pages

- `index.html`
  - Material Guardian privacy policy page for App Store Connect and Google Play
- `terms.html`
  - Material Guardian public terms-of-use page for App Store subscription review and in-app legal links
- `delete-account.html`
  - Material Guardian public account-deletion request page for Google Play's required web deletion link
  - also usable as the optional Apple `User Privacy Choices URL` for Material Guardian
- `fabrication-helper.html`
  - Fabrication Helper privacy policy page for the paid-up-front local toolbox MVP
- `fabrication-helper-terms.html`
  - Fabrication Helper terms and safety notes page

## Internal notes

- `docs/suite_policy_source_of_truth_2026-04-28.md`
  - suite page ownership and app-specific behavior split
- `release/app-store-compliance-checklist.md`
  - working checklist for Apple App Store and Google Play readiness

## Suite release rule

- Material Guardian and Fabrication Helper have different current data/billing behavior, so their public pages should stay app-specific where needed.
- Fabrication Helper's current MVP is a paid-up-front local toolbox with no account, backend entitlement, trial, subscription, cloud sync, ads, analytics SDK, or in-app unlock behavior unless its app repo says otherwise.
- Before any Play Store or App Store submission, compare the app repo's real behavior to the relevant public page and update both if they drift.
