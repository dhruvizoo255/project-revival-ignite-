---
name: project-revival-online-screening
description: Scores PPT-plus-repository submissions for Project Revival against its six published Round 1 criteria, checks existing-project evidence, ranks submissions for a shortlist, and applies an optional capped SDG bonus.
---

# Project Revival Online Screening

## Mission
Rank submissions for Project Revival's online shortlist using the six published Round 1 criteria. Apply the official eligibility and authenticity rules in `references/event-rules.md`. Eligibility is open to undergraduate and postgraduate students across all disciplines. Purely cloned or plagiarized codebases are disqualifying when substantiated under organizer review. Do not confuse legitimate reuse of libraries with plagiarism. The Round 1 submitted codebase becomes the mandatory baseline for Round 2. The official Stage 3 judging breakdown is 60% Custom Feature Implementation and 40% Original Project Depth; this is separate from the Round 1 screening score. The six Round 1 criteria are:
1. Technical depth
2. Code originality
3. System architecture
4. Execution quality
5. Design and creativity
6. Growth potential

This is a competitive ranking, not a generic pass/fail gate. The organizer decides the final shortlist.

## Rules source
Read the `references/event-rules.md` shipped inside this skill folder. If a separately supplied event-rules file is provided, compare its rule version. If versions differ, stop final ranking and ask which version controls. Do not rely on a root file that may not be installed with the skill. The root copy in the bundle is a convenience; all three copies must remain identical.

Do not invent missing eligibility rules, N, cutoff, or tie-breaks. If N is unset, provide provisional rankings only and request organizer confirmation.

## Inputs
Expected: PPT/PDF, repository URL or source bundle, project/team ID, demo/deployment link if available, and contribution/reuse disclosures required by event rules. Extract the repository URL from the PPT where possible. The PPT is the team's narrative; repository and demo evidence are used to validate its claims.

## Evidence and repository inspection protocol
1. Record artifacts, links, reviewer, review date, rule version, branch/commit hash if available, and access status.
2. Inspect PPT claims about problem, features, architecture, tech stack, novelty, demo, and repo.
3. Inspect repository tree, README, dependency/config files, entry points, tests, key implementation files, and history where accessible.
4. If execution is attempted, use an isolated sandbox/container/VM with no real credentials or sensitive files. Do not auto-run install scripts; inspect scripts/dependencies first. Never run untrusted code on the host with secrets. If safe isolation is unavailable, do not execute it.
5. Use the same **8-minute default inspection/run time-box** per submission unless event rules change it before the batch begins. Record commands and outcomes. If execution is not attempted or fails due to environment/API key/database/GPU requirements, mark `unverified-environment`; do not lower the score as if software failure were proven.
6. Compare slide claims against repository/demo evidence in a claims-vs-evidence table.
7. Label claims Verified, Partially verified, Unverified, or Unverified-environment. Never claim to have run code/tests/scans unless actually done.

## Existing-project authenticity
The event expects an existing project. Compare available history to the announcement date specified in event rules. Consider repository creation date, earliest meaningful commits, progression across commits, releases/issues/PRs, prior demos, package releases, and independent dated evidence. A new repository or one large initial commit is a review flag, not proof of misconduct: migrations, squashed history, mirrors, and private transfers can be legitimate. Apply automatic ineligibility only if published rules explicitly say so and evidence satisfies them. Ask for clarification within the cure period.

## Code originality method
Assess project-specific logic, algorithms, workflows, integrations, engineering choices, and the team's implementation contribution. Compare PPT claims to observable code and history. Check attribution/disclosures for major reused components. Libraries, frameworks, pretrained models, templates, tutorials, and AI-assisted code are not inherently disqualifying; apply the exact policy in event rules. Do not accuse a team of plagiarism from similarity alone. Uncertain provenance is a concern for organizer review, not a proven finding.

## Base score — 100 points
Scores must be **whole numbers only**. Apply the anchors proportionally to each category maximum and avoid double-penalizing a single weakness.

General anchors, expressed as a percentage of category maximum:
- **0–19%:** no credible evidence or core claim contradicted.
- **20–39%:** weak/superficial; little implementation evidence.
- **40–59%:** adequate baseline with notable gaps.
- **60–79%:** strong and coherent evidence with limited gaps.
- **80–99%:** exceptional for the cohort, technically convincing and well-supported.
- **100%:** outstanding evidence across the criterion; use sparingly.

1. **Technical depth — 25:** meaningful technical problem-solving, algorithms/models/systems/data/integrations and trade-offs; do not privilege AI over other domains.
2. **Code originality — 20:** distinctive team contribution, project-specific logic/integration, appropriate attribution, and transparency about reuse.
3. **System architecture — 15:** coherent modules, data/control flow, separation of concerns, interfaces, and justified technology choices; compare PPT diagrams to code.
4. **Execution quality — 15:** implementation evidence and completeness relative to claims, reproducible demo, tests/error handling where appropriate. Separate environment failure from software failure.
5. **Design and creativity — 15:** suitability and thoughtfulness of UX, interaction design, creative approach, and design/demo evidence; don't reward decoration alone.
6. **Growth potential — 10:** credible path to further development, extensibility, adoption, users, or impact grounded in the actual project.

## Optional SDG bonus — +0 to +2
Only assess if a team claims alignment or a credible connection is apparent. No claim means +0, no penalty. Event focus: SDGs 4, 8, 9, 11, 12, 17.
- +0: no credible causal link; no penalty.
- +1: plausible, specific connection between actual functionality and a named focus SDG.
- +2: clear, supported connection with responsibly qualified impact claims.
A label/icon alone is not evidence. Do not require measured societal impact from a student prototype. SDG alignment is never an eligibility gate.

## Ranking and calibration
- **Total = base score (0–100) + SDG bonus (0–2). Rank descending by total /102.** If total scores tie, apply the tie-break order confirmed in event rules. Recommended order: technical depth, code originality, architecture, execution quality, design/creativity, growth potential.
- If N is not set, return a provisional ranking and request it; do not invent a cutoff.
- If repo access is unavailable, private without access, or evidence is too incomplete to score fairly, put the submission in a **clarification/review queue**. Do not automatically rank it last. Apply the published cure period and then rescore with the same rules.
- Before the full batch, calibrate on 3–5 varied sample submissions. Have organizers review score rationales and adjust anchors/policy once, before batch scoring. Freeze the rubric and event-rule version. Then score all submissions using the frozen rubric. Do not change anchors mid-batch except through a documented, cohort-wide correction.
- Borderline, disputed originality, and possible rule violations require a second reviewer.

## Output
Use `templates/screening-report.md` for each submission and `templates/leaderboard.md` for batch ranking. Include metadata, PPT-vs-code table, authenticity review, six scores with rationale, optional bonus, total /102, rank/recommendation, confidence, clarification queue, and organizer-only notes. Keep reviewer speculation private and team messages neutral.

## Fairness
Use identical time-boxes and evidence standards. Do not privilege a stack, school, team size, polished slides, number of commits, or deployment unless event rules say otherwise. Separate missing evidence from proven failure. Organizers make final decisions.
