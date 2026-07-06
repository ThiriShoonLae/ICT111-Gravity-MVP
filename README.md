# Gravity

## Course Information
Course Code: ICT111
Course Name: Introduction to Information Technology
Instructor: Dr. Herison Surbakti
Project Type: 14-Labs Continuous IT Startup MVP Development

## Team Name
Gravity

## Team Members and Roles
| Student ID | Name | Role | Responsibility |
|---|---|---|---|
| 6704806 | Hein Htet Aung | Product Lead + Documentation Lead | Define problem, target users, value proposition; maintain README and logbook |
| 6610285 | Thiri Shoon Lae Oo | UX/UI Lead + Validation Lead | Design wireframes and user flow; run customer discovery and collect evidence |
| 6602963 | Eimyat Yadanar Mon | Technical and Business Lead | Manage repository structure and prototype feasibility, business aspects |

## Initial Problem Area
Our team is interested in **how RSU students buy and sell used items when they move in and out of university**. Students who are leaving, graduating, or moving dorms need to clear furniture, appliances, textbooks, and other items quickly, while new and continuing students want those same things cheaply. Today this happens in scattered Facebook and LINE groups where listings are buried, unsearchable, and disorganised. We want to build a simple student-only marketplace that connects buyers and sellers directly.

## Target Users
Rangsit University students in two roles: **sellers** who are moving out, graduating, or leaving (especially international students) and need to clear their belongings, and **buyers** who are new or continuing students looking for cheap used furniture, appliances, and textbooks. During opportunity scanning the team also considered a degree progress tracker, a shared expense splitter, and a content planner, but selected the student marketplace because the problem is real and recurring, and we belong to the user group, which makes validation easy.

## Selected IT Venture Direction
After Lab 2 opportunity scanning, our team selected **Gravity**, a **peer-to-peer student marketplace**. The target users are RSU students who need to sell or buy used items when moving in or out, and who currently rely on messy, unsearchable Facebook and LINE groups. The platform connects buyers and sellers directly — sellers post listings, buyers browse, search, and filter, and the platform then connects the two parties so they finish the deal themselves. We deliberately do **not** hold inventory or process payments, which keeps the build feasible and avoids any advanced cybersecurity. A simple AI assistant helps sellers write listings and lets buyers search in natural language. To keep the marketplace trusted, access is limited to verified RSU students using a university email plus a one-time in-person student ID check (no ID card images are stored). This idea scored highest on our NUF matrix (New 3, Useful 5, Feasible 5 = 13).

## Customer Problem Discovery (Lab 03)
In Lab 3, our team collected early problem evidence from target users to confirm whether the problem we selected in Lab 2 is real and important, not just team opinion.

**Target Respondents.** We focused on RSU students who buy or sell used items around moving in or out: graduating and leaving students, new and continuing students, international students, and dorm residents. We gathered 15 early responses through a short survey and brief interviews (recorded in `/data/raw-responses.xlsx`).

**Main Evidence Found.** The strongest, most repeated pattern was scattered, unsearchable buy/sell channels (11 of 15 respondents), followed by usable items being given away or discarded under time pressure (7 of 15) and measurable time loss of about 30–90 minutes per item. Current workarounds are Facebook groups, LINE chats, word of mouth, and noticeboards. A trust and safety concern about meeting strangers also appeared.

**Updated Problem Statement.** RSU students who move out at the end of a term — especially graduating and international students — lose time and money trying to sell used furniture, appliances, and textbooks through scattered, unsearchable Facebook and LINE groups, and often give items away or discard them; new and continuing students struggle to find affordable used versions in time and end up buying new.

**Decision for Next Step.** The problem is confirmed as real and recurring, so we keep the direction but **narrow the target segment** to movers dealing with higher-value items, and we will add a safer contact step to the planned solution. Full details are in `/docs/customer-discovery-summary.md`, `/docs/problem-notes.md`, `/docs/assumption-evidence-table.md`, and `/docs/customer-questions.md`.

## Technology Possibility
Possible technologies:
- Web application
- Mobile application
- Dashboard
- AI-assisted feature
- Cloud-based system
- IoT-supported system
- Cybersecurity tool
- SaaS platform
- Marketplace or digital platform

Most likely for our MVP: a **web application + marketplace/digital platform**, with a simple cloud-based data store (Google Sheet or a lightweight database) for listings, plus an optional AI-assisted feature for listing help and natural-language search.

## Repository Structure
- **docs**: reports, team profile, idea log, weekly logbook, and problem notes
- **prototype**: source code or clickable prototype files
- **data**: survey responses, validation data, and metrics
- **finance**: financial assumptions and model
- **diagrams**: user flow and technical architecture diagrams
- **screenshots**: evidence of prototype and repository progress
- **pitch**: pitch deck and final demo files

## Weekly Progress Log
| Lab | Main Activity | Output | Status |
|---|---|---|---|
| Lab 1 | Lab setup and idea log | Repository, team profile, initial idea log, weekly logbook | Completed |
| Lab 2 | IT opportunity scanning | Opportunity scan, NUF scoring sheet, selected opportunity | Completed |
| Lab 3 | Customer problem discovery | Customer questions, problem notes, response data, assumption-evidence table, discovery summary | Completed |

## Current Status
In Lab 3, we ran customer problem discovery for Gravity. We defined our target respondents, prepared non-leading discovery questions, and collected 15 early responses from students who buy and sell used items when moving. We separated our assumptions from the evidence, identified the repeated pain points (scattered channels, time loss, discarded items, and trust concerns), and wrote an evidence-based updated problem statement. The evidence confirms the problem is real, so we are keeping the direction and narrowing the target segment.

## Next Step
In Lab 4, we will define our customer segment and persona in detail and write user stories based on the discovery evidence, then begin turning the validated problem into MVP requirements.
