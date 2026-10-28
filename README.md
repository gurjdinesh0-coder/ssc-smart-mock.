# SSC Smart Mock — prototype v2.1 (OCR-enabled)

A mobile-friendly, offline-first SSC mock test PWA prototype. Features include:
- SSC CHSL, CGL, MTS, GD, CPO and custom practice labels
- Subject-wise and mixed sample tests
- Custom test timers, question palette, mark-for-review and auto-submit
- Local saving of tests and attempts in the browser
- Photo upload and on-device OCR using Tesseract.js, with editable extracted text; English/Hindi language selection

## Important limits
- Photo OCR is not a full AI question understanding system. It reads text and makes a best-effort conversion of clearly labelled A/B/C/D choices. Always review question text, choices, answer keys and explanations before saving.
- Tesseract.js and its language data are loaded from a CDN on first OCR use, so the first OCR run requires internet. Core mock tests and saved data work offline after the app is loaded. OCR may need internet again if the browser clears its cache.
- No AI answer-generation service or official answer-key verification is connected in this prototype. Questions without a known answer are left unscored until you provide the correct answer.
- Browser local storage is local to that browser profile. Clearing site data can delete saved tests and history; export/backup is not included yet.
- This is a PWA project, not a compiled APK. The Android APK must be packaged and tested separately.

## Android-only setup route
1. Download and extract the ZIP on your Android phone using a file manager such as Files or ZArchiver.
2. Publish the contents of this folder to an HTTPS static host. One route is to create a GitHub repository in your mobile browser, upload `index.html`, `manifest.json`, `sw.js`, and `icon.svg`, then enable GitHub Pages in repository Settings → Pages. Wait for the HTTPS site URL.
3. Open the HTTPS site in Chrome on Android, use the browser menu → **Add to Home screen** / **Install app**, then open it from the home screen. This installs the PWA, not yet a standalone APK.
4. To create an APK, open PWABuilder (https://www.pwabuilder.com/) in the mobile browser and enter the published HTTPS URL. Follow its Android package instructions. If its workflow requires a downloadable signing/build artifact or desktop tooling, use a trusted Android cloud build service or a computer for that final step; do not install unknown APKs from unofficial sources.
5. Test offline mode, photo selection, OCR after first load, timers, saved tests, and results before relying on it for exam practice.

## OCR format that converts best
For best automatic structuring, photos should clearly show questions and choices labelled `A)`, `B)`, `C)`, `D)`. If an answer key is visible, it should say something like `Answer: B`. OCR output is placed into the editable question text area; verify before saving.
