# Peer Review Report

> **Instructions:** Complete this form **individually and independently**.
> Do not discuss your ratings with teammates before submitting.
> Submit via EEClass as a **separate, confidential submission** — not in the shared team repo.
> Your teammates will not see this report.
>
> Reference the team's `WORK_ALLOCATION_TEMPLATE.md` when completing this form.

---

## Your Details

| Field | Your answer |
|-------|------------|
| Full Name | 梁易軒 |
| Student ID | 112707003 |
| Team ID | 23 |
| Date submitted | 2026-06-11 |

---

## Rating Scale

| Rating | Meaning |
|--------|---------|
| **5** | Exceeded expectations — delivered more than agreed; helped teammates; consistently high quality |
| **4** | Met expectations fully — delivered exactly what was agreed; on time; good quality |
| **3** | Mostly met expectations — minor shortfalls; one or two items completed late or with help |
| **2** | Partially met expectations — noticeable gaps; teammates had to cover some tasks |
| **1** | Did not meet expectations — significant tasks left incomplete; very limited contribution |

---

## Section A — Self-Assessment

### A1. What did you personally implement?

List the specific tasks, functions, files, or document sections that you were the primary author of.
Be specific (e.g., "I designed all 12 tables in schema.sql and implemented query_national_rail_availability and execute_booking").

> *Your answer:*
> In addition to leading the advanced extension track, I actively co-authored and implemented the core graph database (Neo4j) layer. For **Task 4 and Task 5**, I wrote and optimized essential Cypher query functions within `databases/graph/queries.py`, formulated path-traversal logic, and assisted in building the graph schema seeding pipeline (`seed_neo4j.py`). 
> 
> Furthermore, I was the primary author of **Task 6 (Optional Extension)**, where I independently designed and implemented the "Live Disruption & Adaptive Routing Engine." This involved creating the `station_disruptions` operational table with a production-grade partial index in PostgreSQL, as well as engineering the dynamic node isolation and adaptive routing mechanism using `apoc.algo.allSimplePaths` in Neo4j. I also authored the automated integration test script (`test_disruption.py`) and fully documented **Section 7** and **Section 5 (Examples 4-5)** of the Design Document.
---

### A2. What challenges did you face?

Describe any technical or collaboration difficulties you personally encountered and how you resolved them.

> *Your answer:*
> One of the major challenges was collaboration and team dynamics during the initial phase. Because the team members did not know each other beforehand, we faced a high communication barrier. 
> 
> Due to this lack of familiarity, our initial work allocation for the database implementation was poorly structured and somewhat uncoordinated. This resulted in a highly ambiguous ownership definition within the codebase; for instance, it was completely unclear who was primarily responsible for implementing the graph routing logic in `graph/queries.py`. This lack of clarity led to overlapping work, disjointed division of labor, and integration friction when we began coding the database functions.
> 
> To resolve this, I actively initiated a mid-project adjustment to recalibrate our project scope and clear up the ownership mess. I decided to step up and take full, independent ownership of the complex Task 6 extension track (Live Disruption & Adaptive Routing Engine) from scratch. This strategic realignment successfully decoupled my tasks from the ambiguous core query dependencies, allowing my teammates to focus entirely on stabilizing the core modules they had already started, which eliminated further collaboration friction and maximized team throughput.


---

### A3. Self-rating

| Criterion | Rating (1–5) | Justification (1–2 sentences) |
|-----------|-------------|-------------------------------|
| I delivered the tasks assigned to me in the work allocation | 4 |Despite the initial uncoordinated work allocation within the team, I fully delivered my adjusted coding responsibilities for the database project. |
| The quality of my work was satisfactory | 4 | I successfully engineered advanced features like partial indexing and custom Neo4j path filtering that met all local runtime constraints. |
| I communicated well and kept the team informed | 4 | I proactively flagged the code ownership issues early on and continually updated my teammates on my independent Task 6 progress via GitHub.|
| I met deadlines agreed within the team | 4 |I completed all my implementation, testing, and documentation tracks ahead of the final deployment deadline. |
| **Overall self-rating** | 5 |While I met standard expectations on regular tasks, I took the initiative to design and implement the complex Task 6 extension from scratch to actively pursue bonus point opportunities for the team. |

---

### A4. Estimated contribution percentage

What percentage of the total team effort do you estimate you personally contributed?

> My estimated contribution: **__25__%**

---

## Section B — Peer Assessments

Complete one subsection per teammate. Add or remove subsections to match your team size.
If your team has 2 members, complete B1 only. If 3 members, complete B1 and B2.

---

### B1. Assessment of Teammate 1

| Field | Your answer |
|-------|------------|
| Teammate's full name |周怡辰 |
| Teammate's student ID | 112401541 |

#### What did this teammate deliver?

List the tasks, functions, files, or document sections that this teammate was the primary author of,
based on what you observed during the project (compare against the work allocation).

> *Your answer:*

#### Did their actual contribution match the agreed work allocation?

> *Your answer (Yes / Mostly / Partially / No — with explanation):*

#### Peer rating for this teammate

| Criterion | Rating (1–5) | Justification (1–2 sentences) |
|-----------|-------------|-------------------------------|
| Delivered the tasks assigned in the work allocation | | |
| Quality of their work was satisfactory | | |
| Communicated well and kept the team informed | | |
| Met deadlines agreed within the team | | |
| **Overall rating for this teammate** | | |

#### Estimated contribution percentage for this teammate

> My estimate of their contribution: **__50__%**

---

### B2. Assessment of Teammate 2

| Field | Your answer |
|-------|------------|
| Teammate's full name | 林誼婷 |
| Teammate's student ID | 112102010 |

#### What did this teammate deliver?

> *Your answer:*

#### Did their actual contribution match the agreed work allocation?

> *Your answer (Yes / Mostly / Partially / No — with explanation):*

#### Peer rating for this teammate

| Criterion | Rating (1–5) | Justification (1–2 sentences) |
|-----------|-------------|-------------------------------|
| Delivered the tasks assigned in the work allocation | | |
| Quality of their work was satisfactory | | |
| Communicated well and kept the team informed | | |
| Met deadlines agreed within the team | | |
| **Overall rating for this teammate** | | |

#### Estimated contribution percentage for this teammate

> My estimate of their contribution: **__25__%**

---

## Section C — Contribution Percentage Summary

All members (including yourself) must sum to 100%.

| Member | Your estimated % | Notes |
|--------|----------------|-------|
| Yourself | % | |
| Teammate 1 | % | |
| Teammate 2 | % |  |
| **Total** | **100%** | |

---

## Section D — Overall Team Reflection

### D1. What went well in the team's collaboration?

> *Your answer (2–4 sentences):*

---

### D2. What would you do differently if you did this project again?

> *Your answer (2–4 sentences):*

---

### D3. Is there anything else the markers should know about team dynamics or individual contributions?

This is optional. Use it only if there is important context that the ratings above do not capture
(e.g., a member had a documented personal emergency, or a member was unresponsive for a significant period).

> *Your answer (or "Nothing to add"):*

---

## Declaration

I confirm that this peer review reflects my honest and independent assessment.
I understand it will be kept confidential from my teammates.

**Signed:** _________________________________ **Date:** _______________
