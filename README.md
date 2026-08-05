# 2FA Generator

Offline-capable TOTP secret & QR code generator. Runs entirely in your browser — secrets never leave your device.

**Version:** `1.1.0`

## Live site

https://rh77-sudo.github.io/2FA_Generator/

## Features

- Generate strong Base32 secrets with `crypto.getRandomValues` (256-bit)
- Encode `otpauth://` QR codes for Google Authenticator / Apple Passwords
- Live 6-digit TOTP preview (30s timer)
- English / 中文 UI
- **Fully offline** after first download (local CSS + libraries, no CDN)
- Secrets are not written to disk, localStorage, or remote servers
- Sensitive DOM cleared on tab close / navigation

## Run locally

Open `index.html` (or `2FA_Generator.html`) in a browser. No build step, no server required.

```
index.html
2FA_Generator.html   # same app
vendor/
  app.css
  qrcode.min.js
  otpauth.umd.min.js
```

## Privacy notes

- Crypto and QR encoding run client-side only
- App Store / Play download links need the internet if you use them; generating keys does not
- Clipboard copy is optional (OS clipboard history is outside this app)

## License

MIT
