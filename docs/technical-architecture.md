# Technical Architecture — Gravity

## Project Title
Gravity — RSU Student Secondhand Marketplace

## 1. Selected Prototype Platform
**Frontend + localStorage/JSON** — HTML/CSS/JavaScript web app where listing data is seeded from a JSON dataset (converted from `/data/sample-listings.csv`) and all user actions (new listings, status changes, contact requests) are stored in the browser's localStorage.

## 2. Architecture Decision
This platform fits the team, the timeline, and the requirements:

- **Continuity:** it extends the Lab 05 wireframe (`/prototype/wireframe/`) directly — the same HTML/CSS becomes the final prototype's interface, so no work is thrown away and the final build stays aligned with the graded wireframes.
- **Skill match:** the team's strengths are HTML/CSS, basic JavaScript, documentation, and data design. A PHP/MySQL or Firebase backend would add server setup, hosting, and security work that risks the timeline without adding graded value (implementation realism rule).
- **Requirement coverage:** localStorage + JSON can genuinely demonstrate every fixed requirement — input (FR-03), storage (FR-04 explicitly allows local storage/JSON), list/search/detail (FR-05–07), status (FR-08), admin update (FR-09), validation/feedback (FR-10–11), and a dashboard computed from the same data (FR-12).
- **Zero-cost deployment:** the prototype can go live on GitHub Pages from the same repository, giving a real URL for the demo and for QR-code channel testing.

## 3. Main Components

| Component | Description | Tool / Technology | Related Requirement |
|---|---|---|---|
| User Interface | Mobile-first screens carried over from the Lab 05 wireframe (home, browse, sell, detail, dashboard, admin, register) | HTML + CSS | FR-01, FR-02, FR-13, FR-14 |
| Data Input Form | Create Listing form with required-field validation and confirmation messages | HTML form + JavaScript validation | FR-03, FR-10, FR-11 |
| Data Storage | Seed dataset in JSON (from sample-listings.csv); user-created records and updates persisted in browser localStorage | JSON file + localStorage API | FR-04 |
| Record List | Listings rendered from storage with search box and category filter | JavaScript (render + filter functions) | FR-05, FR-06 |
| Detail View | Per-listing page/section showing full fields, verified badge, status, contact request button | JavaScript (render by listing ID) | FR-07, FR-15 |
| Admin Function | Admin screen: update listing status, remove listing, approve verification (list-based demo) | JavaScript writing back to localStorage | FR-09, FR-08 |
| Dashboard / Summary | Counts by status and category computed live from the stored records | JavaScript aggregation | FR-12 |

## 4. What Will Be Fully Implemented?
- Create listing (form → validation → saved to localStorage → appears in list) — the full FR-02 primary pathway.
- Listings list with working keyword search and category filter.
- Detail view rendered from the stored record.
- Status lifecycle: Available → Reserved → Sold, updated by seller/admin and reflected everywhere immediately.
- Admin actions: update status, remove listing (with confirmation).
- Validation and confirmation messages on all forms.
- Dashboard computed from live data (totals, per-status, per-category).
- Mobile-responsive layout.

## 5. What Will Be Simulated?
- **RSU email verification:** the format check (@rsu.ac.th) is real; the actual email confirmation link and the in-person ID check are simulated with a "verified" flag the admin can toggle.
- **Contact reveal after mutual agreement:** with no backend, two browsers cannot notify each other in real time. The demo shows both sides from one browser: buyer sends a request → the seller/admin view accepts it → contact details unlock. State is stored locally.
- **Photo upload:** placeholder image areas (no file storage in localStorage at realistic sizes).
- **Multi-user accounts:** one demo "logged-in" user per role (buyer / seller / admin) switched via the interface, instead of real authentication.

## 6. Final Prototype Risk
**Biggest risk:** localStorage data is per-browser — during the demo, data could look inconsistent if screens are opened in different browsers, or a browser reset could wipe demo records.
**Mitigation:** the app always seeds from the JSON dataset on first load (so a wipe self-heals to a known state), a "Reset demo data" button restores the seed instantly, and the demo runs from one prepared browser. Secondary risk — JavaScript scope creep — is mitigated by freezing features to F01–F12 (the Must/Should list); anything else goes to GitHub issues as post-course work.
