# Random

**TL;DR:** This repo holds one Google Sheets Apps Script file from 2019 with three helper functions: look up a place's details (address, phone, rating, opening hours) from Google Maps, find a place's ID from free text, and copy a sheet of beers into a Firebase database. It is a saved snippet, not a project.

## What's in here

| Path | What it is |
|---|---|
| `AppsScript for sheets` | The script (63 lines): `GET_DETAILS(id)` and `locId(text)` as custom sheet functions using the Google Places API, and `writeDataToFirebase()`, which reads beer name, country, type, style and places from the first sheet and writes them to a Firebase Realtime Database. |
| `.code-inventory/` | A machine-written index of the repo (added September 2026). |

The API key, sheet ID and database URL are placeholders (`YOUR_PLACES_API_KEY` and so on), so nothing secret is committed. To use it, paste the script into a sheet's Apps Script editor and fill those in.

## Status

One content commit (2019-04-01) and one automated index commit (2026-09-06).
