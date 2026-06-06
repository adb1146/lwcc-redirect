# lwcc-redirect

A one-page **OAuth redirect bridge** for the LWCC Injured Worker Companion mobile app
(SMART-on-FHIR, Epic).

Epic's sandbox patient login completes redirects only to `https://` URLs, not to a custom app
scheme. This static page is registered as the app's Epic redirect URI. Epic redirects here with
`?code=...&state=...`; the page immediately forwards that exact query into the app's deep link
(`lwcc://redirect?...` on iOS, `intent://...;scheme=lwcc;...` on Android). The app's auth session
watches the `lwcc://` scheme and completes the sign-in.

- Served at: `https://adb1146.github.io/lwcc-redirect/`
- No secrets here. The authorization `code` is single-use, short-lived, and useless without the
  app's PKCE `code_verifier` (which never leaves the device). Tokens never transit this page.
- This page only ever forwards to the fixed `lwcc://redirect` target.
