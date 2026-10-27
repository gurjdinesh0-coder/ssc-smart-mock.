# SSC Smart Mock — first prototype

An offline-first, mobile-friendly Progressive Web App (PWA) prototype for SSC practice.

## Included
- SSC CHSL, CGL, MTS, GD, CPO and custom practice selectors
- Four SSC-style subject areas and sample MCQs
- Custom sectional timer, question palette, mark-for-review, auto-submit
- Results and answer explanations
- Local saved tests and history
- Manual question editor and bulk text parser
- Photo attachment preview for reference
- PWA manifest and service worker for install/offline caching

## Important limitations in this prototype
- Photo OCR / AI conversion is not implemented yet. The attached image is a reference; type or paste the extracted questions in the editor.
- The sample questions are demonstrations, not an official or comprehensive SSC question bank.
- Negative marking, exam-specific official patterns and configurable marks per question are not implemented yet.
- Data is stored in this browser's local storage. Clearing browser data removes it.
- A signed native APK is not included. This is a PWA that can be installed from a secure-hosted URL in Android Chrome. To make an APK, package the app with a native Android wrapper (e.g. Trusted Web Activity or WebView) and build/sign it with Android tooling.

## Run locally
Serve this folder over localhost or HTTPS (service workers do not run from file://). For example, with Python installed:

    python -m http.server 8000

Then open http://localhost:8000 in a browser. For Android installation, deploy to an HTTPS host, open the URL in Chrome, then use the browser menu's Install app / Add to Home screen option.
