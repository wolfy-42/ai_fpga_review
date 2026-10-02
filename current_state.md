<!-- SPDX-License-Identifier: MIT -->
`SPDX-License-Identifier: MIT`

# Current State: fpga review

_Last updated: 2026-10-01 21:24 (America/Toronto)_

## Update rule

- Update this file once the last batch of tasks is finished and the project has been idle for 15 minutes.
- To do this, schedule one reminder per batch and never delete or reset reminders. A reminder that finds newer activity does nothing.
- Each update replaces the "Snapshot" section below and bumps the "Last updated" date.
- This is also rules 1 and 1.1 in `claude/rules.md`.

## Snapshot

**1. Status:** The project setup is in progress. No design has been shared or reviewed yet.

**2. Project files** (all start with the SPDX MIT license header)

**2.1** `claude/claude.md` is the entry point. It points to `rules.md` and `current_state.md`.

**2.2** `claude/rules.md` holds rules 1–13 and Appendix RVU Rules. Rule 13: conflicts and open items about the rules go in `rules_conflicts.md`, numbered OI.N / OI.N.M. Rule 12: every review report is produced as both `.md` and `.xlsx` at the same time. Rule 8.4 sets where review reports are stored (`claude/reviews/fpga_review_report_<design>_<YYYY-MM-DD>.md`). Rule 11 defines the 6-column review results table; rule 11.7 says the template already contains it. Appendix RVU Rules has sections RVU.0–RVU.8, and every major section has at least one rule.

**2.2.1** RVU.0: execute it last; a 5-column table with one row per major section (section ID, title, % compliant, % minor non-compliant, % major non-compliant). Not-applicable items are excluded from the totals.

**2.2.2** RVU.1 Pre-requisites: RVU.1.1 Requirements Document (unique IDs, one or two lines per requirement), RVU.1.2 FPGA Project Creation TCL Scripts, RVU.1.3 Simulation with SIMU, RVU.1.4 Simulation/Verification Test Plan and Report, RVU.1.5 Validation Lab Test Plan and Report (plan only or report only = minor), RVU.1.6 Lab Testing Automation Python Scripts, RVU.1.7 Compliance Matrix.

**2.2.3** RVU.2 Documentation: RVU.2.1 PL Documentation (RVU.2.1.1–RVU.2.1.5), RVU.2.2 Architecture Documentation (RVU.2.2.1–RVU.2.2.4), RVU.2.3 Project Documentation (RVU.2.3.1–RVU.2.3.2). All graded present and complete = compliant, incomplete = minor, missing = major.

**2.2.4** RVU.3 RTL Review: RVU.3.1 Coding Guidelines (followed = compliant; not followed = major; third-party coding rules took precedence = not-applicable), RVU.3.2 Clock Distribution (no chaining = compliant; chained with jitter in range = minor; out of range = major), RVU.3.3 Reset Generation and Distribution (reset IP or PLL/DLL lock = compliant; otherwise minor), RVU.3.4 CDC/RDC, RVU.3.5 FSM Usage (simple flip-flop pipeline = compliant), RVU.3.6 Control Plane with SystemRDL.

**2.2.5** RVU.4 3rd Party Synthesis: RVU.4.1 MATLAB to HDL Generation and RVU.4.2 HLS Flow (each not-applicable if the design doesn't use MATLAB / HLS).

**2.2.6** RVU.5 Simulation-Verification: RVU.5.1 Coding Guidelines (same grading as RVU.3.1), RVU.5.2 Simulation Methodology (SIMU or SSVE-like = compliant; UVM = minor; none = major), RVU.5.3 SSVE AI Project Check (no or minor discrepancies = compliant; otherwise major).

**2.2.7** RVU.6 PaR and STA: RVU.6.1 Constraints Files Organization (no constraints files = major), RVU.6.2 I/O Timing Constraints for Clocked Pins.

**2.2.8** RVU.7 Lab Debug-Integration-Validation: RVU.7.1 Coding Guidelines (same grading as RVU.3.1), RVU.7.2 Python Functional Checks Against Requirement IDs. RVU.8 Deliverables: RVU.8.1 Checklist Items in Project Output Products.

**2.3** `claude/template_fpga_review_report.md` has the same sections and subsections as Appendix RVU Rules, the pre-built RVU.0 scores table, and a 6-column results table with one empty row under each of the 34 RVU items. Every item has an intent and a pre-filled Description (column 2).

**2.4** `claude/review_open_items.md` holds only open items about the design under review, numbered ROI.N / ROI.N.M with a separate sequence per project under review (rule 6.1). So far only the "General" heading exists: ROI.1 (first design to review). Highest number used under General: ROI.1.

**2.4.1** `claude/rules_conflicts.md` holds the open items about the rules: OI.4, OI.5.1, OI.6 and OI.12 (SIMU/SSVE repo links and details, SSVE AI project, coding guidelines). Highest number used: OI.12. On 2026-10-01 at 21:20 OI.1–OI.3, OI.5.2 and OI.7–OI.11 were closed with D's answers: duplicate checks kept and reworded with "Scope:" lines (RVU.1 checks use, later sections check content), D enters results columns 4–5 during the review (rule 11.5.1), all-N/A sections show N/A in RVU.0, the template's Description column is pre-filled from the rules, the Excel and .md reports go in the Mac repo `reviews/` folder (rule 12), and the major-section intent lines were removed from the template.

**2.5** `claude/archive/` holds the backups.

**2.6** On 2026-10-01 the review-section numbering was renamed from `R.N` to `RVU.N`, and "Appendix R" was renamed to "Appendix RVU Rules", in all project files.

**2.7** On 2026-10-01 the former RVU.2 TPL Documentation and RVU.3 Architecture Documentation were merged into RVU.2 Documentation (as RVU.2.1 and RVU.2.2), RVU.2.3 Project Documentation was added, and the later sections were renumbered: RVU.3 RTL Review, RVU.4 3rd Party Synthesis, RVU.5 Simulation-Verification, RVU.6 PaR and STA, RVU.7 Lab Debug-Integration-Validation, RVU.8 Deliverables.

**2.7.1** On 2026-10-01 at 21:06 a Coding Guidelines check was inserted as the first item of RVU.3, RVU.5 and RVU.7; the existing items there moved down by one (RVU.3.1–3.5 → 3.2–3.6, RVU.5.1–5.2 → 5.2–5.3, RVU.7.1 → 7.2).

**2.8** Terms: PL = Project Lead (spelled out at first use, in the RVU.2.1 heading; renamed from TPL / Technical Project Lead on 2026-10-01). CDC = clock domain crossing, RDC = reset domain crossing (RVU.3.4). FSM = finite state machine (RVU.3.5). HDL Coder = MATLAB/Simulink HDL generation tool; SysGen = System Generator (RVU.4.1). HLS = high-level synthesis (RVU.4.2). SIMU and SSVE: repos under https://github.com/wolfy-42/ (exact links and SSVE meaning are OI.4 and OI.5.1).

**2.9** On 2026-10-01 at 20:10 another session also wrote backups to `claude/archive/` and removed older ones, so more than one session may be editing this project.

**3. Local copy and git**

**3.1** The project files are copied to the Mac at `~/writing/github_wolfy-42_simu-documentation/ai_fpga_review`, which is a git repo on branch `main`. Commit author: `wolfy-42 <168792347+wolfy-42@users.noreply.github.com>`.

**3.2** Remote: `origin = git@github.com:wolfy-42/ai_fpga_review.git`. Commits on `main`: "Initial commit", "Add FPGA review project files", "Add SPDX MIT license header to all files", `0bcae0d` "Rename review numbering to RVU and add review rules" (all pushed), and `d83fa2b` "Resolve open items, add coding guidelines checks and report tables" (2026-10-01 21:08).

**3.3** `d83fa2b` is committed locally but not pushed: the session sandbox on the Mac has no SSH keys for GitHub. D is to push it from their own Terminal (`git push`).

**3.4** The local copies aren't synced automatically with the project files. They only change when D asks for them to be copied again. Commit `d83fa2b` predates `rules_conflicts.md` and rule 13 (2026-10-01 21:13).

**4. In progress:** nothing.

**5. Open items:** see `claude/review_open_items.md`.
