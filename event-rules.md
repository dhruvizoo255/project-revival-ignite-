# Project Revival — Event Rules (Organizer Configuration)

**Rule version:** PR-2026-v1-draft  
**Status:** DRAFT — organizer must complete fields marked `REQUIRED` before final screening  
**Last updated:** 18 October 2026  
**Rule owner / approver:** REQUIRED

## Round 1 — Online screening

- **Event announcement date (for existing-project check):** REQUIRED — enter exact date and time zone.
- Submission artifact: PPT plus repository URL/source access.
- Required PPT fields: REQUIRED — list the required fields.
- Repository access policy: REQUIRED — choose public repo, private repo with reviewer access, ZIP, or permitted combination.
- Deployed demo mandatory?: REQUIRED — yes/no.
- Existing-project eligibility rule: REQUIRED — define what evidence qualifies and any exceptions. Do not automatically reject solely on repo creation date or a squashed/single commit.
- AI-tool policy: REQUIRED — allowed / prohibited / disclosure required / other.
- Reuse policy: REQUIRED — rules for open-source code, tutorials, templates, pretrained models, and attribution.
- Required eligibility criteria: REQUIRED — quote the published rules.
- **Number of teams advancing (N): REQUIRED.**
- **Tie-break order (recommended default):** higher technical depth, then code originality, system architecture, execution quality, design and creativity, growth potential. Organizer must confirm or replace before screening.
- Clarification/cure period for missing evidence: REQUIRED — specify deadline and whether teams can supply access or evidence.
- **Repository inspection run time-box:** 8 minutes per submission (draft recommendation; organizer may change before the batch begins).
- Calibration sample size: 3–5 submissions before full batch scoring.
- SDG bonus: optional, outside base 100, capped at +2, never an eligibility requirement.
- Event SDG focus: 4, 8, 9, 11, 12, 17.

## Round 2 — Offline project revival

- Event date: 22 October 2026 (confirm).
- Overall event window: 10:00–16:00 (confirm).
- Challenge handout/briefing duration: REQUIRED.
- Stage 3 demo and defense window: REQUIRED.
- Breaks/setup time: REQUIRED.
- **Actual active coding window:** REQUIRED — calculate after handout, setup, breaks, testing buffer, and demo/defense are excluded.
- **One common challenge tier for the cohort:** REQUIRED — choose Tier A or Tier B only after confirming active coding time. Do not assign different tiers to teams in the same cohort unless organizers explicitly approve an exception and calibrate effort.
- Default tier mapping:
  - Tier A — focused integration, 1–2 effort points.
  - Tier B — bounded end-to-end feature, 2–3 effort points; use only if active coding time is at least 4 hours and dependencies are low risk.
  - Tier C — not used by default for this event; requires explicit organizer approval and a separate calibration.
- Team size limits: REQUIRED.
- Allowed internet / AI tools / APIs: REQUIRED.
- Credentials and external services supplied: REQUIRED.
- Required deliverables: branch or commit, test evidence, short demo, and technical explanation (confirm/adapt).
- Challenge approver: REQUIRED.
- Stage 3 judging rubric: defined by organizers/judges; the challenge-design skill does not impose one.

## Ranking and SDG policy

- **Ranking uses total score out of 102** = base score out of 100 + optional SDG bonus out of 2.
- Sort descending by total score. If totals tie, apply the confirmed tie-break order above to the base-criterion scores.
- SDG bonus is applied before tie-breaks because it is part of total score; it cannot change eligibility or rescue a weak submission. If organizers prefer bonus-only tie-breaking, change this policy before screening and update every artifact consistently.
- No SDG claim means +0 bonus and no penalty.

## Consistency and safety

- Freeze this file and its rule version before scoring the batch.
- Both skills use the copy of this file in their own `references/event-rules.md` folder when installed separately. Keep all three copies byte-for-byte identical.
- Do not run untrusted code on a host with real credentials or sensitive files. Use an isolated sandbox/container/VM, disable access to secrets, avoid auto-running install scripts, and inspect dependency scripts before execution. If safe isolation is unavailable, do not run the code; review statically and mark execution as not attempted.
- Unset REQUIRED fields must be completed by organizers. The skill must not invent them.


## Official eligibility and contest rules (organizer-provided)

- **Eligibility:** Open to undergraduate (Bachelor's) and postgraduate (Master's) students across all disciplines.
- **Project authenticity:** Submitted projects must represent original, genuine work by the team. Purely cloned or plagiarized codebases will be disqualified. Investigate concerns using evidence and organizer review; do not treat similarity, use of libraries, or a single commit as proof by itself.
- **Codebase constraint:** Shortlisted teams must build upon the exact codebase submitted during Round 1. Building a completely new project during Round 2 is strictly prohibited. Preserve the Round 1 repository reference/commit or archive so judges can compare the starting and final code.
- **Custom feature execution:** Teams must adhere to the bespoke feature challenge assigned by organizers. Challenge briefs must specify required behavior and acceptance criteria.
- **SDG and impact integration:** Teams are encouraged to highlight real-world applicability, scalability, technological sustainability, and relevant UN SDG alignments during live defense. SDG alignment remains optional and is never a Round 1 eligibility condition or mandatory challenge requirement. The event's focus SDGs are 4, 8, 9, 11, 12, and 17.
- **Judges' authority:** Decisions made by judges and the organizing committee across all stages are final and non-contestable.

## Official Stage 3 evaluation — 100% total

- **Custom Feature Implementation — 60%**
  - Technical implementation and functionality
  - Integration with the existing codebase
  - Innovation, code quality, and modularity
  - Execution and delivery within the sprint timeframe
- **Original Project Depth — 40%**
  - Originality and technical maturity
  - System architecture and complexity
  - User experience, completeness, and stability

These are the official Stage 3 evaluation categories supplied by the organizer. Do not replace them with another compulsory judging rubric. Judges may apply their own detailed scoring within these categories. The challenge designer may provide optional checklists mapped to these categories only when requested.

## Exact-codebase verification for Round 2

- Record the Round 1 submitted repository URL and, where possible, branch/commit hash or source archive checksum.
- The challenge brief must explicitly state that the team must extend that submitted codebase.
- At final submission, compare the team's starting codebase with its result and check that the assigned feature is integrated into the original project.
- A rewrite or new project presented instead of the submitted codebase violates the stated rule. If a repository was migrated, mirrored, or history was squashed before Round 1, use the preserved Round 1 snapshot as the baseline.
- Escalate suspected violations to organizers/judges with evidence; do not make unsupported accusations.
