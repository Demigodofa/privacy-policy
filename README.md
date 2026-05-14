# privacy-policy

Public policy source for Welders Helper suite store and in-app privacy disclosures.

This repo is the canonical public policy/static-page repo for shared Welders Helper language plus per-app overlays. Keep app behavior truth in the app repo, but keep public privacy, terms, account-deletion, and store-disclosure pages here so Apple/Google release work does not drift across apps.

Commit and push coherent GitHub checkpoints after policy wording, app page, store-disclosure, or release-checklist changes so every machine sees the same public policy truth.

## Pages

- `apps.html`
  - Fabrication Helper-only public app page for the current no-ads, one-time-purchase promotion; do not lump Material Guardian into this campaign yet
- `index.html`
  - Material Guardian privacy policy page for App Store Connect and Google Play
- `material-guardian.html`
  - Material Guardian public landing page for the demo video, App Store and Google Play links, and ad traffic
- `terms.html`
  - Material Guardian public terms-of-use page for App Store subscription review and in-app legal links
- `support.html`
  - Material Guardian support URL page with account, subscription, scanning, export, and deletion support contact details
- `delete-account.html`
  - Material Guardian public account-deletion request page for Google Play's required web deletion link
  - also usable as the optional Apple `User Privacy Choices URL` for Material Guardian
- `fabrication-helper.html`
  - Fabrication Helper privacy policy page for the paid-up-front local toolbox MVP on Android and iOS
- `fabrication-helper-app.html`
  - Fabrication Helper public landing page for App Store, Google Play, screenshots, and shop-facing promo copy
- `fabrication-helper-terms.html`
  - Fabrication Helper terms and safety notes page
- `fabrication-helper-support.html`
  - Fabrication Helper App Store Support URL page with paid-download, calculator workflow, privacy, and safety-support contact details

## Internal notes

- `docs/suite_policy_source_of_truth_2026-04-28.md`
  - suite page ownership and app-specific behavior split
- `release/app-store-compliance-checklist.md`
  - working checklist for Apple App Store and Google Play readiness
- `promo/`
  - Fabrication Helper promo source files, post copy, QR flyer, and social image render notes

## Suite release rule

- Material Guardian and Fabrication Helper have different current data/billing behavior, so their public pages should stay app-specific where needed.
- Fabrication Helper's current MVP is a paid-up-front local toolbox with no account, backend entitlement, trial, subscription, cloud sync, ads, analytics SDK, or in-app unlock behavior unless its app repo says otherwise.
- 2026-05-13 Fabrication Helper promo state: current promotion priority is Fabrication Helper because it is available on both iOS/App Store and Android/Google Play at a one-time `$4.99` price with no ads. Phone/social links should use `fabrication-helper-app.html` plus direct App Store and Google Play links; Material Guardian should not be bundled into this promotion yet. Public flyer/social assets live under `assets/promo/`, with source files and post copy in `promo/`.
- 2026-05-06 Fabrication Helper iOS state: bundle ID `com.weldershelper.fabricationhelper.ios`, App Store app shell created, and signed IPA upload succeeded through `altool`. Privacy behavior still matches the local-toolbox page: selected-tool preferences use local storage; calculator/reference inputs stay on device; no camera, location, contacts, microphone, analytics, or account backend in the current app.
- 2026-05-06 Material Guardian iOS App Review metadata correction: added `support.html` so App Store Connect can use a dedicated Support URL instead of pointing support traffic at the privacy policy root.
- 2026-05-11 Material Guardian Apple review cleanup: privacy, support, terms, and delete-account pages now use store-neutral subscription wording so App Store Connect-facing pages do not reference Google Play unless a platform-specific page intentionally does.
- 2026-05-14 Material Guardian availability update: Material Guardian is now publicly reachable on both App Store and Google Play. The landing page should send traffic to `https://apps.apple.com/us/app/material-guardian/id6764147952` and `https://play.google.com/store/apps/details?id=com.asme.receiving`.
- Before any Play Store or App Store submission, compare the app repo's real behavior to the relevant public page and update both if they drift.
