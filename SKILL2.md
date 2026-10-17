---
name: project-revival-challenge-designer
description: Converts approved Round 1 submissions into one fair, codebase-specific offline feature challenge, calibrated to actual build time and a common cohort difficulty tier.
---

# Project Revival Offline Challenge Designer

## Mission
Design one bespoke, technically meaningful feature challenge for each shortlisted project. Teams must build upon the exact codebase submitted during Round 1; building a completely new project is strictly prohibited. The brief must explicitly state this constraint and define how judges can verify integration with the original codebase. Reuse the approved Round 1 report and verified findings; do not re-audit the entire repository unless new evidence affects the chosen task.

## Rules source and handoff
Read `references/event-rules.md` shipped inside this skill folder. If another rules file is supplied, compare rule versions and resolve conflicts with the organizer. The bundle-root copy is a convenience only; keep all three copies identical.
Use the Round 1 screening report, PPT, repository URL, and verified capability notes as inputs. If the handoff is missing, do a concise audit and note that fact.

## Active build time
The overall event window is currently 10:00–16:00, but this includes briefing/handout, setup, breaks, testing, demo preparation, and Stage 3 demos/defense. Never assume six hours of coding. Use the active coding window from event rules. If it is unset, ask the organizer before finalizing; a provisional plan may assume 3 active build hours, clearly labelled as an assumption.

## One common tier for the cohort
Use the single cohort-wide tier specified in event rules. Do not independently assign a different tier to each team by default. Tailor the feature to each codebase while keeping effort, uncertainty, and proof burden comparable.

- **Tier A — Focused integration:** 1–2 effort points; one focused component with a clear interface.
- **Tier B — Bounded end-to-end feature:** 2–3 effort points; use only when at least 4 active coding hours are confirmed and dependencies are low risk.
- **Tier C:** disabled by default; only if organizer explicitly enables and calibrates it.
- Effort points are relative, not exact hours. Do not use 5-point tasks for this event by default.

## Lightweight workflow
1. Reuse the Round 1 report's verified project summary, stack, strengths, and unknowns.
2. Identify natural extension points and avoid rewrites.
3. Generate three candidate challenges. For each, state the user/engineering value, likely integration point, risk, effort points, and demo proof.
4. Rank using 0–10 scores: impact 35%, relevance 25%, feasibility 20%, demonstrability 20%.
5. Select one primary challenge aligned to the cohort tier and active build time. Include only essential supporting requirements, one optional stretch goal, and fallback scope.
6. Make acceptance criteria observable; include a happy path, edge/failure case, regression check, and a short demo sequence.
7. Keep the team-facing brief to about one page. Candidate ranking and organizer-only rationale must not be sent to teams.

## Optional SDG context
Event focus SDGs are 4, 8, 9, 11, 12, 17. SDG alignment is optional and never an eligibility requirement. Add a brief organizer-only note only when the project has a genuine connection. Consider an SDG-deepening feature only if it naturally fits the project's purpose and does not make workload or judging less fair. Do not force-fit SDGs or invent impact claims.

## Official rules and Stage 3 boundary
Teams must adhere to the bespoke feature challenge and continue from the exact Round 1 submitted codebase. Include the original repository URL and baseline commit/archive reference in organizer-only notes, and state the codebase constraint in the team-facing brief. Building a completely new project is prohibited.

Judges/organizers own Stage 3 decisions, which are final and non-contestable. The official evaluation breakdown is **60% Custom Feature Implementation** (technical implementation/functionality, integration with existing codebase, innovation/code quality/modularity, execution/delivery within the sprint) and **40% Original Project Depth** (originality/technical maturity, architecture/complexity, UX/completeness/stability). Do not impose a different compulsory rubric. Optional checklists must map to these categories and are only provided when requested.

Teams are encouraged to discuss real-world applicability, scalability, technological sustainability, and relevant SDG alignment during the live defense. SDG alignment is encouraged, not mandatory; do not force an SDG feature into the challenge.

## Output
Use `templates/challenge-brief.md`. Include organizer-only candidate ranking, common cohort tier, effort estimate, active build-time assumption, dependencies, approval/version, and optional SDG note if relevant. Team-facing brief includes objective, required behavior, acceptance criteria, integration boundaries, non-goals, tests, demo proof, fallback/stretch, and submission deliverables.

## Final check
Confirm the cohort tier matches event rules; active build time is real; Round 1 findings were reused; one coherent feature is feasible; requirements are testable; dependencies are available; SDG is not forced; and no new judging or event rules were invented. Organizer approves the final assignment.
