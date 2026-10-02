# Glow Tracker

Glow Tracker is a mobile-first skincare package tracker that stores data in Google Sheets through a Google Apps Script web app.

## Local homepage

This repo is designed to be used as a static homepage / landing page. The app entry point is `index.html`.

## Google Apps Script backend

Copy the contents of `google-apps-script.gs` into a new Apps Script project and deploy it as a web app.

1. Open https://script.google.com
2. Create a new project
3. Paste the contents of `google-apps-script.gs`
4. Save the project
5. In the Apps Script editor, click Deploy -> New deployment
6. Choose type: Web app
7. Execute as: Me
8. Who has access: Anyone
9. Copy the deployed web app URL

Then open the app in a browser and use either:
- the `#s=` URL parameter, for example `https://your-pages-site/#s=YOUR_DEPLOYMENT_ID`
- or paste the full deployed URL into the app when prompted

The app is also compatible with `#s=demo` to try the interface without a spreadsheet.

## Data model

The Apps Script creates three Sheets automatically:
- `Profiles`
- `Packages`
- `Visits`

## Notes

- The app expects a JSON response from the script with `ok`, `profiles`, `packages`, and `visits`.
- If the deployed script URL is missing or invalid, the app now shows the setup flow instead of failing hard.
