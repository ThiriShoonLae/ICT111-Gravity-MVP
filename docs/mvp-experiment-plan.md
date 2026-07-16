# MVP Experiment Plan — Gravity

## 1. Group and Project Information
- Group name: Gravity
- Project title: Gravity — RSU Student Secondhand Marketplace
- Repository link: https://github.com/ruinogenesis/ICT111-Gravity-MVP
- Main target user: RSU student sellers under move-out pressure (persona Su Su); student buyers as secondary users
- Prototype platform: Frontend + localStorage/JSON (per `/docs/technical-architecture.md`)

## 2. Experiment Objective
We want to test whether RSU students can complete the core marketplace workflow — post a listing, find a specific item with search/filter, understand statuses, and understand the reveal-after-agree contact process — without help, and whether they say they would use Gravity instead of Facebook/LINE groups.

## 3. Requirement Scope for the Experiment

| Requirement ID | Requirement Summary | Related Screen/Feature | Tested in This Experiment? |
|---|---|---|---|
| FR-01 | Problem-specific landing screen | Home (F01) | Yes — T1 |
| FR-02 | Primary user pathway | Full flow across screens | Yes — T2–T6 |
| FR-03 | User input / data submission | Create Listing form (F03) | Yes — T2 |
| FR-05 | View records list | Browse listings (F04) | Yes — T3 |
| FR-06 | Search / filter / category | Search + category filter (F05) | Yes — T3 |
| FR-07 | Detail view | Listing detail (F06) | Yes — T4 |
| FR-08 | Status tracking | Status badges (F07) | Yes — T5 |
| FR-10 | Validation | Required-field errors (F10) | Yes — T2 |
| FR-11 | Confirmation / feedback | Success messages (F10) | Yes — T2 |
| FR-15 | Privacy / responsible data | Reveal-after-agree note (F08) | Yes — T6 (comprehension) |
| FR-09, FR-12 | Admin function, dashboard | Admin, Dashboard | No — team-facing; tested internally in the implementation sprint |
| FR-04, FR-13, FR-14 | Storage, consistency, responsive | Cross-cutting | Indirectly — demo runs on localStorage, testers use their phones |

## 4. MVP Experiment Type
Selected experiment type: **Simple web prototype (HTML/CSS/JS with simulated records) combined with a form-based simulation.**

Reason for selection: our riskiest assumptions are about the input/submission workflow (will busy sellers complete a structured form?) and findability (can buyers locate an item quickly?). Per the decision guide, a simple web prototype collects exactly the evidence we need — clickable workflow, stored/simulated records, validation, and feedback messages. It also matches our chosen architecture, so everything learned transfers directly to the implementation sprint (Labs 10–11). The demo is /prototype/mvp-demo.html (link in `/prototype/mvp-demo-link.md`).

## 5. Test Users

| Test User Group | Number of Testers | Why They Are Relevant |
|---|---:|---|
| Graduating / international students (seller side) | 2 | Match the primary persona — real move-out time pressure (E02) |
| First-year or continuing students (buyer side) | 2 | Match the buyer segment searching for cheap used items (CS02) |
| Student with no secondhand-trading experience | 1 | Tests first-time clarity without prior habits |

Tester details: `/data/test-users.csv`. Five testers is the minimum; more is better if time allows before Lab 08.

## 6. Experiment Procedure Summary
Each tester is tested individually for ~10 minutes on their own phone or a laptop: (1) read the opening script (this is not a test of you); (2) tester performs tasks T1–T6 from /docs/experiment-script.md while thinking aloud; (3) observer records completion, time, help needed, and confusion points in `/data/experiment-results.csv`; (4) tester fills the feedback form (`/docs/feedback-form.md` / `/data/feedback-results.csv`); (5) short open discussion. No hints are given unless the tester is fully stuck (recorded as "help needed").

## 7. Expected Learning
After the experiment we will decide, using the rules in `/docs/success-metrics.md`: **build** (metrics met → proceed with the implementation sprint as planned), **revise** (some metrics fail → fix labels, form fields, or flow before building), or **revisit** (most metrics fail → re-examine requirements and user stories against the Lab 03 evidence). We especially expect to learn whether the reveal-after-agree contact concept (our trust differentiator, A-04) is understood or needs redesign.
