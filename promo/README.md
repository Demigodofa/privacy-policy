# Fabrication Helper Promo Assets

Current promotion priority: Fabrication Helper, NO ADS, one-time `$4.99`, available on iOS/App Store and Android/Google Play.

Primary phone/social product page:

`https://demigodofa.github.io/privacy-policy/fabrication-helper-app.html`

Use the direct App Store and Google Play links in phone posts when the channel can hold both links. Keep this campaign focused on Fabrication Helper.

## Source Files

- `fabrication-helper-flyer.html`
  - printable letter flyer source
- `fabrication-helper-social-square.html`
  - 1080x1080 click-first square social/share image source emphasizing NO ADS and one-time purchase
- `fabrication-helper-post-pack.md`
  - copy/paste post text for text messages, Facebook/local trade groups, LinkedIn, shop counter/invoice line, flyer captions, and direct store links
- `fabrication-helper-money-sprint.md`
  - 48-hour revenue checklist with exact channels, links, review ask boundaries, and daily metrics

## Generated Public Assets

- `../assets/promo/fabrication-helper-flyer.pdf`
  - printable 8.5x11 PDF
- `../assets/promo/fabrication-helper-flyer-preview.png`
  - PNG preview of the flyer
- `../assets/promo/fabrication-helper-social-square.png`
  - square image for Facebook, texts, and general sharing; no QR because phone/social viewers need clickable post links
- `../assets/promo/fabrication-helper-qr.png`
  - QR code pointing at the Fabrication Helper product page with flyer UTM tagging for printed material

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
npx -y qrcode "https://demigodofa.github.io/privacy-policy/fabrication-helper-app.html?utm_source=flyer&utm_medium=qr&utm_campaign=fabrication_helper_499" -o assets/promo/fabrication-helper-qr.png
```
