# Fabrication Helper Promo Assets

Current promotion priority: Fabrication Helper, one-time `$4.99`, available on iOS/App Store and Android/Google Play.

Public app hub:

`https://demigodofa.github.io/privacy-policy/apps.html`

## Source Files

- `fabrication-helper-flyer.html`
  - printable letter flyer source
- `fabrication-helper-social-square.html`
  - 1080x1080 square social/share image source
- `fabrication-helper-post-pack.md`
  - copy/paste post text for text messages, Facebook/local trade groups, LinkedIn, shop counter/invoice line, and flyer captions

## Generated Public Assets

- `../assets/promo/fabrication-helper-flyer.pdf`
  - printable 8.5x11 PDF
- `../assets/promo/fabrication-helper-flyer-preview.png`
  - PNG preview of the flyer
- `../assets/promo/fabrication-helper-social-square.png`
  - square image for Facebook, texts, and general sharing
- `../assets/promo/fabrication-helper-qr.png`
  - QR code pointing at the app hub with flyer UTM tagging

Public URLs:

- `https://demigodofa.github.io/privacy-policy/assets/promo/fabrication-helper-flyer.pdf`
- `https://demigodofa.github.io/privacy-policy/assets/promo/fabrication-helper-social-square.png`
- `https://demigodofa.github.io/privacy-policy/assets/promo/fabrication-helper-qr.png`

## Regenerate Assets

Run from the `privacy-policy` repo root:

```powershell
npx playwright pdf --paper-format Letter --viewport-size 816,1056 --wait-for-timeout 500 file:///C:/Users/KevinPenfield/source/repos/Demigodofa/privacy-policy/promo/fabrication-helper-flyer.html assets/promo/fabrication-helper-flyer.pdf
npx playwright screenshot --viewport-size 816,1056 --wait-for-timeout 500 file:///C:/Users/KevinPenfield/source/repos/Demigodofa/privacy-policy/promo/fabrication-helper-flyer.html assets/promo/fabrication-helper-flyer-preview.png
npx playwright screenshot --viewport-size 1080,1080 --wait-for-timeout 500 file:///C:/Users/KevinPenfield/source/repos/Demigodofa/privacy-policy/promo/fabrication-helper-social-square.html assets/promo/fabrication-helper-social-square.png
```
