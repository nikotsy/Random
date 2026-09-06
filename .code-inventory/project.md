# Random

A scratch repository. One commit, April 2019, one file — `AppsScript for sheets` —
holding three Google Apps Script functions written around a personal beer
catalogue kept in a spreadsheet.

**Kind:** playground · **Lifecycle:** dormant

## What is actually here

Two separate ideas share the file:

1. **Google Places, callable from a cell.** `locId(text)` turns free text into a
   Places `place_id`; `GET_DETAILS(id)` takes that id and spills name, latitude,
   longitude, address, phone, rating, price level and opening hours across a row.
   Used as a formula pair in adjacent columns.
2. **Sheet to Firebase.** `writeDataToFirebase()` reads the whole first sheet and
   writes it into a Realtime Database node as an object keyed by the name column,
   so an app can read a hand-maintained spreadsheet as data.

## Technologies

Google Apps Script (JavaScript). Google Sheets. The legacy Google Places API.
Firebase Realtime Database, reached through the third-party `FirebaseApp` Apps
Script library — a dependency that is invisible in the source and has to be added
to the script project by library id before anything runs.

## Worth knowing

- No secrets are committed. The API key, spreadsheet id and database URL are all
  placeholders (`YOUR_PLACES_API_KEY`, `YOUR_GOOGLE_SHEET_ID`,
  `YOUR_FIREBASE_DATABSE_URL` — the typo is in the original).
- The reusable technique in the Places half is the nested-array return
  (`[[a, b, c]]`), which is how one custom-function call fills several cells.
- The Firebase half is positional: column indexes are hard-coded, so inserting a
  column corrupts the export, and each run replaces the whole node rather than
  merging.
- The Places endpoints are the legacy API, since superseded by Places API (New).
  Anything lifted from here needs the endpoint updated.

There is no build, no test, no CI and no README. Treat it as a snippet archive,
not a project.
