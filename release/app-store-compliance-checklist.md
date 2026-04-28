# App Store Compliance Checklist

Date: 2026-04-27

This file maps the current Material Guardian repo state to the public policy and account-deletion
requirements for Apple App Store and Google Play.

## Repos

- mobile app: `/Users/kevinpenfield/Documents/Playground/material-guardian-mobile`
- backend: `/Users/kevinpenfield/Documents/Playground/app-platforms-backend`
- public policy site: `/Users/kevinpenfield/Documents/Playground/privacy-policy`
- operating notes: `/Users/kevinpenfield/kevin-codex`

## Public pages prepared here

- privacy policy: `index.html`
- terms of use: `terms.html`
- account deletion page: `delete-account.html`

These are intended to back:

- Apple App Store Connect `Privacy Policy URL`
- Apple subscription terms link or in-app terms surface
- Apple optional `User Privacy Choices URL`
- Google Play `Privacy policy`
- Google Play account deletion web link

## Current app behavior confirmed from local repos

- Material Guardian stores jobs, reports, photos, scans, signatures, drafts, and export packets locally on-device.
- The Flutter app also supports account-backed features including email-code sign-in, session restore, organization membership, invites, seat management, subscriptions, and entitlement checks.
- The backend contract includes purchase verification routes for both Apple and Google.
- No advertising or analytics SDKs were found in the current mobile dependencies.
- iOS currently declares camera and photo-library usage strings in `ios/Runner/Info.plist`.

## Apple requirements checked

Official sources reviewed on 2026-04-27:

- App Review Guidelines:
  `https://developer.apple.com/app-store/review/guidelines/`
- App privacy details:
  `https://developer.apple.com/app-store/app-privacy-details/`
- App Store Connect app privacy reference:
  `https://developer.apple.com/help/app-store-connect/reference/app-information/app-privacy`
- Account deletion guidance:
  `https://developer.apple.com/support/offering-account-deletion-in-your-app/`

Current Apple-ready items:

- public privacy policy URL exists in this repo
- public terms-of-use URL exists in this repo
- separate public account-deletion page exists in this repo
- the mobile app now links to hosted privacy, terms, deletion, and subscription-management pages
- the mobile app now exposes an in-app delete-account initiation path for signed-in users
- the backend now has `POST /account/delete-request` to mark the user as `deletion_requested` and revoke active sessions
- iOS camera and photo-library purpose strings exist

Apple gaps still remaining in the app or backend:

1. The updated backend deletion route still needs to be deployed to the actual environment used by the shipped iOS build.
2. App Store Connect privacy answers must be completed to match actual account, session, subscription, and organization handling.
3. App Store Connect metadata should point at the final hosted privacy-policy and terms URLs, not local repo paths.
4. Push this repo so the public pages and any final copy edits are actually live on GitHub Pages before submission.

## Google Play requirements checked

Official sources reviewed on 2026-04-27:

- Google Play Developer Program policies:
  `https://support.google.com/googleplay/android-developer/answer/16933379?hl=en`
- Data safety form guidance:
  `https://support.google.com/googleplay/android-developer/answer/10787469?hl=en`
- Account deletion requirement:
  `https://support.google.com/googleplay/android-developer/answer/13327111?hl=en-EN`

Current Google-ready items:

- public privacy policy URL exists in this repo
- public terms-of-use URL exists in this repo
- public web account-deletion page exists in this repo
- the mobile app now includes an in-app account-deletion path for signed-in users
- Android manifest is currently narrowed to camera access and explicitly removes microphone and broad media-storage permissions inherited from plugins

Google Play gaps still remaining in the app or console:

1. The Play Data safety form must disclose backend-held account, session, organization, entitlement, and purchase-related data.
2. The Play Data deletion questions must point to `delete-account.html` or the final hosted equivalent.
3. The Play Console privacy policy field must use the hosted public URL, not a repo URL.
4. Push this repo so the public pages and any final copy edits are actually live on GitHub Pages before release.

## Suggested next code changes outside this repo

### `material-guardian-mobile`

1. Recheck all store-facing copy after the final iOS billing path is enabled in the exact release build.
2. Confirm the release app uses the backend environment where `POST /account/delete-request` is deployed.

### `app-platforms-backend`

1. Decide the full backend deletion workflow and retention policy behind the new delete-request route.
2. Deploy the delete-request route to the environment used by production mobile builds.
3. Make sure purchase, session, and membership retention rules are explicit before release.

## Practical release rule

Do not ship the old local-only privacy-policy wording once account-backed features are present in
the released build.
