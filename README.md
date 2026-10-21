# WEBAURA by iii

A responsive, editorial-style studio website inspired by contemporary Indian craft, built with semantic HTML, Tailwind CDN, vanilla JavaScript, Firebase Web SDK and Vercel static hosting.

## Files
- `index.html` — website, styles, interactions and inquiry form.
- `firebase-config.js` — Firebase web configuration placeholders and central contact settings.
- `firestore.rules` — restrictive public inquiry rules; public users cannot read inquiries.
- `privacy.html`, `terms.html` — starter policy pages; review and adapt before launch.
- `vercel.json` — static deployment headers and clean URLs.

## Run locally
Open `index.html` using a local static server (for example, VS Code Live Server). ES modules and Firebase imports may not work from a `file://` URL.

## Configure Firebase
1. Create or select a Firebase project and register a Web app.
2. Copy the project's Web app configuration into `firebase-config.js`; replace all `YOUR_...` placeholders.
3. Create a Cloud Firestore database.
4. Publish `firestore.rules` in Firebase Console.
5. Test inquiry submission using a non-sensitive test inquiry and inspect Firestore rules behavior.

The Firebase web config is designed for client-side use, but it is not a substitute for security rules. Never place service-account JSON, Admin SDK private keys or other server credentials in this repository. The rules intentionally prevent public reads and updates. Admin dashboard/authentication is not implemented in this starter release; add trusted admin authorization before allowing staff to view or manage inquiries.

## Contact details
The form's fallback email behavior should only be enabled after a verified business email is configured. Update the central `studioContact` settings and corresponding form behavior with the real contact details. Instagram is linked to `@webaura_iii`.

## Deploy to Vercel
Import this GitHub repository in Vercel. It is a static site, so no build command is required; the project root is the output directory. Every push to the connected production branch can trigger a deployment.

## Before launch
- Replace Firebase placeholders and publish rules.
- Add a verified contact email and WhatsApp number if desired.
- Review privacy/terms wording for the actual business and applicable law.
- Add a verified canonical domain, social preview image and sitemap after the domain is known.
- Test the form, keyboard navigation, reduced-motion mode and mobile layouts.
- Portfolio entries are explicitly marked as concept projects; replace them only with approved, accurate case studies.
