<!-- SPDX-License-Identifier: MIT -->
`SPDX-License-Identifier: MIT`

# Current State: fpga review

_Last updated: 2026-10-01 20:45 (America/Toronto)_

## Update rule

- Update this file once the last batch of tasks is finished and the project has been idle for 15 minutes.
- To do this, schedule one reminder per batch and never delete or reset reminders. A reminder that finds newer activity does nothing.
- Each update replaces the "Snapshot" section below and bumps the "Last updated" date.
- This is also rules 1 and 1.1 in `claude/rules.md`.

## Snapshot

**1. Status:** The project setup is in progress. No design has been shared or reviewed yet.

**2. Project files** (all start with the SPDX MIT license header)

**2.1** `claude/claude.md` is the entry point. It points to `rules.md` and `current_state.md`.

**2.2** `claude/rules.md` holds rules 1–11 and Appendix RVU Rules. Rule 11 defines the 6-column review results table. Appendix RVU Rules has sections RVU.0–RVU.8.

**2.2.1** RVU.0: execute it last, after RVU.1–RVU.8; populate it as a 5-column table with one row per major section (section ID, title, % compliant, % minor non-compliant, % major non-compliant).

**2.2.2** RVU.1 Pre-requisites has RVU.1.1 Requirements Document, RVU.1.2 FPGA Project Creation TCL Scripts, RVU.1.3 Simulation with SIMU, RVU.1.4 Simulation/Verification Test Plan and Report, RVU.1.5 Validation Lab Test Plan and Report, RVU.1.6 Lab Testing Automation Python Scripts and RVU.1.7 Compliance Matrix, each with a compliant / minor / major grading rule.

**2.2.3** RVU.2 Documentation: RVU.2.1 Project Lead (PL) Documentation has five document checks (RVU.2.1.1 Checklist Document, RVU.2.1.2 Requirements Document, RVU.2.1.3 Risk Assessment, RVU.2.1.4 Task List Document, RVU.2.1.5 Change Log Document); RVU.2.2 Architecture Documentation has four (RVU.2.2.1 Main Block Diagram, RVU.2.2.2 Architecture Document, RVU.2.2.3 Third-Party IP List, RVU.2.2.4 Logic Size/Resources/Pins Estimation and FPGA Device Selection); RVU.2.3 Project Documentation has two (RVU.2.3.1 Verification Plan for Simulation, RVU.2.3.2 Validation Test Plan for Lab Testing). None of the RVU.2 checks have grading yet (open item 16).

**2.2.4** RVU.3 RTL Review has: RVU.3.1 Clock Distribution (chained PLLs/DLLs = major non-compliant, plus a jitter check against the downstream PLL/DLL allowed input range; rest is open item 19); RVU.3.2 Reset Generation and Distribution (initial reset deassertion via proper reset generation IP or PLL/DLL lock = compliant; rest is open item 20); RVU.3.3 CDC/RDC (vendor IP or pre-existing library = compliant; no library = major non-compliant); RVU.3.4 FSM Usage (FSMs = compliant; no FSMs = major non-compliant; simple flip-flop pipelines excepted, grade is open item 21); RVU.3.5 Control Plane with SystemRDL (SystemRDL = compliant; not SystemRDL = major non-compliant).

**2.2.5** RVU.5 Simulation-Verification has RVU.5.1 Simulation Methodology (SIMU or SSVE-like = compliant; no methodology like SSVE or UVM = major non-compliant; rest is open item 23) and RVU.5.2 SSVE AI Project Check of the Simulation Environment (no or minor discrepancies = compliant; otherwise major non-compliant; details are open item 24).

**2.2.6** RVU.6 PaR and STA has RVU.6.1 Constraints Files Organization (separated by constraint type = compliant; one file or a few unorganized files = minor non-compliant; rest is open item 22) and RVU.6.2 I/O Timing Constraints for Clocked Pins (input setup/hold and output "after" constraints present = compliant; missing = major non-compliant).

**2.2.7** RVU.7 Lab Debug-Integration-Validation has RVU.7.1 Python Functional Checks Against Requirement IDs (used = compliant; otherwise major non-compliant).

**2.2.8** RVU.8 Deliverables has RVU.8.1 Checklist Items in Project Output Products (all checklist items available = compliant; otherwise major non-compliant).

**2.2.9** RVU.4 3rd Party Synthesis has RVU.4.1 MATLAB to HDL Generation (MATLAB with Simulink and HDL Coder, SysGen or similar, with both the MATLAB/Simulink code and the generated HDL available = compliant; either code missing, or MATLAB without direct HDL generation and manually coded RTL = major non-compliant) and RVU.4.2 HLS Flow (HLS with C simulation test cases and TCL/Python build scripts = compliant; anything missing = major non-compliant). The grade for designs that don't use MATLAB or HLS is open item 25.

**2.2.10** Every major section RVU.1–RVU.8 now has at least one rule.

**2.3** `claude/template_fpga_review_report.md` has the same sections and subsections as Appendix RVU Rules. Intents provided so far: RVU.0, RVU.1.1–RVU.1.7, RVU.2.1–RVU.2.3 with all their sub-items, RVU.3.1–RVU.3.5, RVU.4.1–RVU.4.2, RVU.5.1–RVU.5.2, RVU.6.1–RVU.6.2, RVU.7.1 and RVU.8.1.

**2.4** `claude/review_open_items.md` has open items 3, 4, 6–8, 11–17 and 19–25. The highest number used so far is 25.

**2.5** `claude/archive/` holds the backups.

**2.6** On 2026-10-01 the review-section numbering was renamed from `R.N` to `RVU.N`, and "Appendix R" was renamed to "Appendix RVU Rules", in all project files.

**2.7** On 2026-10-01 the former RVU.2 TPL Documentation and RVU.3 Architecture Documentation were merged into RVU.2 Documentation (as RVU.2.1 and RVU.2.2), RVU.2.3 Project Documentation was added, and the later sections were renumbered: RVU.3 RTL Review, RVU.4 3rd Party Synthesis, RVU.5 Simulation-Verification, RVU.6 PaR and STA, RVU.7 Lab Debug-Integration-Validation, RVU.8 Deliverables.

**2.8** Terms: PL = Project Lead (spelled out at first use, in the RVU.2.1 heading; renamed from TPL / Technical Project Lead on 2026-10-01). CDC = clock domain crossing, RDC = reset domain crossing (RVU.3.3). FSM = finite state machine (RVU.3.4). HDL Coder = MATLAB/Simulink HDL generation tool; SysGen = System Generator (RVU.4.1). HLS = high-level synthesis (RVU.4.2). SIMU and SSVE: not defined yet (open items 13 and 23).

**2.9** On 2026-10-01 at 20:10 another session also wrote backups to `claude/archive/` and removed older ones, so more than one session may be editing this project.

**3. Local copy and git**

**3.1** The five files are copied to the Mac at `~/writing/github_wolfy-42_simu-documentation/ai_fpga_review`, which is a git repo on branch `main`. Commit author: `wolfy-42 <168792347+wolfy-42@users.noreply.github.com>`.

**3.2** Remote: `origin = git@github.com:wolfy-42/ai_fpga_review.git`. Local `main` is GitHub's "Initial commit" (LICENSE, README.md) plus 2 commits: add project files, and add SPDX headers.

**3.3** D is to push from their own Terminal (`git push`). Whether the push has happened isn't confirmed yet.

**3.4** The local copies aren't synced automatically with the project files. They only change when D asks for them to be copied again. None of the 2026-10-01 changes have been copied to the local repo yet.

**4. In progress:** nothing.

**5. Open items:** see `claude/review_open_items.md`.
