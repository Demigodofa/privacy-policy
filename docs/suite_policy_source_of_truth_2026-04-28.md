# Suite Policy Source Of Truth

Date: 2026-04-28

## Purpose

This repo holds public privacy, account-deletion, terms, and store-disclosure statements for Welders Helper suite apps.

The goal is one durable place to manage shared language while still allowing each app to have its own disclosures when behavior differs.

## Rule

- Put shared Welders Helper policy language here.
- Put per-app public policy pages here when an app needs different disclosures.
- Keep implementation details in the app repo.
- Before Play Store or App Store submission, compare the app's actual behavior to this repo and update both if they drift.
- Store Console answers should be checked against this repo plus the app repo before submission.

## Current App Split

### Material Guardian

Current public pages:

- `index.html`
- `terms.html`
- `delete-account.html`

Current behavior to keep aligned:

- email-code sign-in
- backend-managed account, session, organization, seat, trial, entitlement, and subscription status
- Google Play subscription handling on Android
- local-first jobs, reports, photos, scans, signatures, and exports unless the user explicitly exports or shares
- camera access only when user starts photo or scan capture
- no contacts or location access in the current Android release

### Fabrication Helper

Current public pages:

- `fabrication-helper.html`
- `fabrication-helper-terms.html`

Current Android MVP behavior to keep aligned:

- paid-up-front local toolbox
- no account, sign-in, backend entitlement, trial, or in-app unlock
- local selected-tool preferences
- calculator/reference inputs processed locally
- no ads or analytics SDKs
- no camera, contacts, microphone, location, broad file storage, or cloud sync in the current MVP

If Fabrication Helper later adds company cloud records, WPS/WPQ/PQR modules, accounts, export/share, or in-app unlocks, add or update the corresponding public pages before release.

## Store Release Rule

Do not treat this repo as static legal boilerplate.

Before a release, re-check:

- app permissions
- account creation and deletion
- local vs backend/cloud data boundaries
- store billing and subscription behavior
- support contact and developer identity
- data safety/privacy declarations
- screenshots and store metadata accuracy
