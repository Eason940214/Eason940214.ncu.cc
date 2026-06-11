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
| The quality of my work was satisfactory | 3 | I successfully engineered advanced features like partial indexing and custom Neo4j path filtering that met all local runtime constraints. |
| I communicated well and kept the team informed | 3 | I proactively flagged the code ownership issues early on and continually updated my teammates on my independent Task 6 progress via GitHub.|
| I met deadlines agreed within the team | 3 |I completed all my implementation, testing, and documentation tracks ahead of the final deployment deadline. |
| **Overall self-rating** | 4 |While I met standard expectations on regular tasks, I took the initiative to design and implement the complex Task 6 extension from scratch to actively pursue bonus point opportunities for the team. |

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
> She was the primary author responsible for the foundational database architecture and theoretical documentation of the project. She successfully designed the core relational schema (`schema.sql` for Task 1) and implemented the complete PostgreSQL user authentication queries (`login_user`, `register_user`, and password security functions for Task 2d). She also built the primary data ingestion pipelines, specifically authoring the PostgreSQL seeding logic (`seed_postgres.py` for Task 3) and the Neo4j graph schema seeding architecture (`seed_neo4j.py` and `seed.cypher` for Task 4). 
> 
> For the **Design Document**, she authored the majority of the theoretical framework and design justifications, specifically delivering **Section 1** (ER Diagram), **Section 2** (Normalisation Justification), **Section 3** (Graph Database Design Rationale), and **Section 4** (Vector / RAG Design).

#### Did their actual contribution match the agreed work allocation?

> *Your answer (Yes / Mostly / Partially / No — with explanation):*
> > **Yes.** Despite the communication barriers we faced as a randomly formed team of strangers, actual contributions fully matched the final agreed work allocation. She delivered the foundational database schemas, authentication logic, and seeding pipelines on time and with high quality, ensuring the rest of the team had a stable database to work with.

#### Peer rating for this teammate

| Criterion | Rating (1–5) | Justification (1–2 sentences) |
|-----------|-------------|-------------------------------|
| Delivered the tasks assigned in the work allocation |5 |She fully delivered all foundational schema setups and database seeding files assigned to her. |
| Quality of their work was satisfactory |4 |The structured data population and ingestion pipelines performed well during standard deployment tests. |
| Communicated well and kept the team informed |4 |Communication was initially restricted by team unfamiliarity, but she maintained standard updates as coding progressed. |
| Met deadlines agreed within the team |4 |She aligned her deliveries well with the team's schedule, ensuring no blocking issues on foundational code. |
| **Overall rating for this teammate** |4 |She was a solid and responsible team member who provided a highly functional database infrastructure for the rest of our tasks. |

#### Estimated contribution percentage for this teammate

> My estimate of their contribution: **__45__%**

---

### B2. Assessment of Teammate 2

| Field | Your answer |
|-------|------------|
| Teammate's full name | 林誼婷 |
| Teammate's student ID | 112102010 |

#### What did this teammate deliver?

> *Your answer:*
> > She was the primary developer responsible for implementing the complex relational business logic and core graph query features of the project. She successfully developed the entire suite of transactional write operations for **Task 2c**, specifically engineering the critical booking engine (`execute_booking`) and its rollback logic (`execute_cancellation`). She was also the primary author of **Task 2a and 2b**, coding essential PostgreSQL read-queries for rail availability, fares, seat mapping, and user profiles.
> For the **Design Document**, she authored **Section 5** (AI Tool Usage Evidence) by compiling Examples 1 to 3, and completely drafted **Section 6** (Reflection & Trade-offs), evaluating the architecture's system design compromises.

#### Did their actual contribution match the agreed work allocation?

> *Your answer (Yes / Mostly / Partially / No — with explanation):*
> **Mostly.** She successfully developed and delivered all the core transactional business logic and relational query modules assigned to her with great code quality. The only minor deviation was during the initial phase, where uncoordinated team planning led to an ambiguous overlap regarding ownership of `graph/queries.py`. However, this was resolved smoothly once we adjusted the project scope and reassigned tasks.
#### Peer rating for this teammate

| Criterion | Rating (1–5) | Justification (1–2 sentences) |
|-----------|-------------|-------------------------------|
| Delivered the tasks assigned in the work allocation |4 |She successfully delivered the heavy transactional booking queries and relational modules assigned to her. |
| Quality of their work was satisfactory | 3 |While the core write queries function correctly, initial integration tests revealed minor edge-case shortfalls that required subsequent team refinement. |
| Communicated well and kept the team informed | 3 |Due to working as strangers initially, progress updates regarding the codebase were somewhat passive and less transparent during mid-project phases. |
| Met deadlines agreed within the team | 3 |Some of her core business logic modules experienced minor delays, which temporarily extended our integration and testing timeline. |
| **Overall rating for this teammate** | 4 |Despite minor shortfalls in communication and minor timeline delays, she remained a competent developer who successfully completed her primary core responsibilities. |

#### Estimated contribution percentage for this teammate

> My estimate of their contribution: **__30__%**

---

## Section C — Contribution Percentage Summary

All members (including yourself) must sum to 100%.

| Member | Your estimated % | Notes |
|--------|----------------|-------|
| Yourself | 25% |Task 6 加分功能實作、撰寫圖形資料庫、設計文件的理論論述（Sec 5-7） |
| Teammate 1 | 45% |負責Seeding腳本撰寫、Neo4j演算法、協助修改queries、撰寫圖形資料庫、設計文件的理論論述（Sec 1-4） |
| Teammate 2 | 30% | 主要負責PostgreSQL核心查詢模組、撰寫圖形資料庫、協助修改Seeding腳本撰寫、設計文件的理論論述（Sec 5-6） |
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
