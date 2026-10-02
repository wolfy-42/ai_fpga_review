<!-- SPDX-License-Identifier: MIT -->
`SPDX-License-Identifier: MIT`

# Project Rules: fpga review

These are the rules for running this project, as set by D. Every new rule gets added to this numbered list. Follow all of them in every session.

**1.** **Keep `current_state.md` up to date after an inactivity timeout.** Update `current_state.md` with the current state (what's done, what's in progress, open issues and next steps) once the last batch of tasks is finished and the project has been idle for 15 minutes. The rule is also written in that file.

**1.1** **How it's done:** after each batch of tasks, schedule one reminder for 15 minutes later. Never delete or reset reminders. When a reminder goes off, check for activity since it was set. If there was activity, do nothing, because a newer reminder already covers it. If there wasn't, update `current_state.md`.

**2.** **Store all project rules in `rules.md`.** Whenever D gives a rule for how to run the project, add it to this file as the next numbered item.

**3.** **Read before changing, and back up the old version.** Before changing any project file, read its current content first. Then save that previous version as a backup in the `archive` folder inside the same project folder as the original (for example `claude/archive/`), named `<filename>_<YYYY-MM-DD_HHMM>.<ext>.bak` in America/Toronto time: the original name with a timestamp, then its extension, then `.bak` (for example `claude/archive/notes_2026-09-28_2054.md.bak` for `claude/notes.md`). Only then write the change.

**3.1** **Exception:** don't make backups of `claude/rules.md`, `claude/current_state.md` or `claude/claude.md`. Still read them before changing them.

**3.2** **Keep at most 3 backups per file.** Each original file can have up to 3 backup files. When a new backup would make 4, delete the oldest one.

**4.** **Review-section rules go in Appendix RVU Rules.** Rules for reviewing a specific section of a review go in Appendix RVU Rules, numbered to match the review: RVU.N covers review section RVU.N, and RVU.N.M covers subsection RVU.N.M (and so on for deeper levels). When reviewing a section, apply every rule under its RVU.N entry, including those in its subsections.

**5.** **Hierarchical numbering.** Everything in the project is numbered hierarchically: 1., 1.1, 1.1.1 and so on, going as deep as needed. This covers rules, review sections, appendix entries and any other numbered lists. Appendix RVU Rules and the review sections use the same scheme with the prefix `RVU`: RVU.1, RVU.1.1, RVU.1.1.1.

**6.** **Track open items in `review_open_items.md`.** Store every open item, conflict and piece of missing information in `claude/review_open_items.md` as a numbered list.

**6.1** **Open-item numbers only go up and are never reused.** Number open items in sequence, always taking the next number after the highest one ever used. When an item is closed, remove it from the list, but never give its number to another item.

**7.** **Never assume, never fill in content.** Use only information D has given. Don't generate, infer or fill in content from general knowledge or assumptions. If something needed is missing or unclear, leave it empty and log it as an open item under rule 6.

**8.** **Run the review in Appendix RVU Rules order, one line at a time.** Run the review following the sequence of the sections and subpoints in Appendix RVU Rules.

**8.1** Every line in Appendix RVU Rules is a separate execution of the rule written on that line.

**8.2** Capture the result of each execution in `fpga_review_report.md`, in the matching section or subpoint.

**8.3** `fpga_review_report.md` starts as a copy of `template_fpga_review_report.md`, which gives it its original structure.

**8.4** Each review report is stored in the project at `claude/reviews/fpga_review_report_<design>_<YYYY-MM-DD>.md`, where `<design>` is the reviewed design's name and the date is the review date (America/Toronto).

**9.** **The template mirrors Appendix RVU Rules.** `template_fpga_review_report.md` is a copy of the sections in Appendix RVU Rules, with exactly the same numbering (RVU.0, RVU.1, RVU.1.1 …). Any discrepancy between the two is flagged as a conflict in `review_open_items.md` (rule 6).

**10.** **"help" / "menu" command.** When D types `help` or `menu`, list the example command prompts below.

**10.1** `execute review`: runs the full review (rule 8).

**10.2** `execute review of section RVU.3`: runs the review of section RVU.3 only. Any section number can be used, for example RVU.N or RVU.N.M.

**11.** **Review results table.** In the review results document (`fpga_review_report.md`), every reviewed item is recorded as a row of a table with these columns:

**11.1** **Column 1, Item number:** the item's RVU number (for example RVU.1.1).

**11.2** **Column 2, Description:** the description of the item being reviewed, the steps to carry out its review, and the grading definition.

**11.3** **Column 3, Result:** the result after executing the review steps, including the grading level, which is one of: `not-applicable`, `compliant`, `minor non-compliant`, `major non-compliant`.

**11.4** **Column 4, Correction:** whether the item has to be corrected or will be left uncorrected.

**11.5** **Column 5, Days to correct:** how many days it will take to correct the item.

**11.6** **Column 6, Issue description:** the description of the issue discovered.

**11.7** `template_fpga_review_report.md` already contains this table, with the column headers and one empty row per RVU item, so each new report starts with it ready to fill in.

**12.** **Always produce the review report as Markdown and Excel.** Every time the review report is generated or updated, produce it in two formats at the same time: `fpga_review_report_<design>_<YYYY-MM-DD>.md` and `fpga_review_report_<design>_<YYYY-MM-DD>.xlsx`, with the same content (rule 8.4 for the name and location, rule 11 for the results table).

---

## Appendix RVU Rules

Rules for reviewing each section of the review, numbered to match it: RVU.N covers review section RVU.N, and RVU.N.M covers subsection RVU.N.M.

### RVU.0 Review Scores
Execute RVU.0 last, after all the other review sections (RVU.1–RVU.8) are completed, even though it comes first in Appendix RVU Rules order (this overrides rule 8 for RVU.0 only).

Populate RVU.0 as a table with one row per major review section (RVU.1, RVU.2, … RVU.8) and these 5 columns:
- Column 1, Section ID: the major section's RVU number (for example RVU.1).
- Column 2, Section title: the title of that section (for example Pre-requisites).
- Column 3, % compliant: the percentage of the section's total items graded `compliant`.
- Column 4, % minor non-compliant: the percentage of the section's total items graded `minor non-compliant`.
- Column 5, % major non-compliant: the percentage of the section's total items graded `major non-compliant`.

Items graded `not-applicable` are excluded from a section's total items, so the three percentages add up to 100%.

### RVU.1 Pre-requisites

#### RVU.1.1 Requirements Document
Check: has a requirements document been used, with each requirement under a unique ID and one or two lines long?
- Requirements document with unique requirement IDs and requirements one or two lines long used: `compliant`.
- A document with another structure used for the requirements (for example an architecture document): `minor non-compliant`.
- Neither of the above used: `major non-compliant`.

#### RVU.1.2 FPGA Project Creation TCL Scripts
Check: have FPGA project creation TCL scripts been used?
- TCL scripts used: `compliant`.
- Scripts other than TCL used: `minor non-compliant`.
- No project creation scripts used: `major non-compliant`.

#### RVU.1.3 Simulation with SIMU
Check: has simulation been performed with SIMU?
- SIMU used: `compliant`.
- Simulation performed with other scripts and methodology: `minor non-compliant`.
- No simulation performed: `major non-compliant`.

#### RVU.1.4 Simulation/Verification Test Plan and Report
Check: have a simulation/verification test plan and a simulation/verification test report been used?
- Simulation/verification test plan and test report used: `compliant`.
- Only a simulation/verification test report made, without a test plan: `minor non-compliant`.
- Only a simulation/verification test plan made, without a test report: `minor non-compliant`.
- No simulation/verification test plan and no test report: `major non-compliant`.

#### RVU.1.5 Validation Lab Test Plan and Report
Check: have a validation lab test plan and a validation lab test report been used?
- Validation lab test plan and test report used: `compliant`.
- Only a validation lab test report made, without a test plan: `minor non-compliant`.
- Only a validation lab test plan made, without a test report: `minor non-compliant`.
- No validation lab test plan and no test report: `major non-compliant`.

#### RVU.1.6 Lab Testing Automation Python Scripts
Check: have lab testing automation Python scripts been used?
- Python lab testing scripts used: `compliant`.
- Non-Python lab testing scripts used: `minor non-compliant`.
- No scripting used for lab testing: `major non-compliant`.

#### RVU.1.7 Compliance Matrix
Check: is there a compliance matrix document that links the verification test cases and the validation test cases to the requirement IDs, and shows which requirements are not covered?
- Compliance matrix links both verification and validation test cases to requirement IDs and shows the requirements not covered: `compliant`.
- Compliance matrix exists but is incomplete: `minor non-compliant`.
- No compliance matrix: `major non-compliant`.

### RVU.2 Documentation
_No rules yet._

#### RVU.2.1 Project Lead (PL) Documentation
One check per PL document below. Grading for each check: document present and complete = `compliant`; present but incomplete = `minor non-compliant`; missing = `major non-compliant`.

##### RVU.2.1.1 Checklist Document
Check: is there a checklist document listing all deliverables for the project?

##### RVU.2.1.2 Requirements Document
Check: is there a requirements document listing the requirements, each under a unique ID and one or two lines long?

##### RVU.2.1.3 Risk Assessment
Check: is there a risk assessment containing:
- a feasibility assessment, with risk assessment and mitigation strategies;
- two risk graphs of risk severity (low / medium / high) vs. risk probability (low / medium / high): one before mitigation, and one after mitigation is implemented.

##### RVU.2.1.4 Task List Document
Check: is there a task list document with effort estimates per task?

##### RVU.2.1.5 Change Log Document
Check: is there a change log document, maintained throughout project execution, logging all changes against the initial requirements together with their effort impact (positive or negative)?

#### RVU.2.2 Architecture Documentation
One check per architecture document below. Grading for each check: document present and complete = `compliant`; present but incomplete = `minor non-compliant`; missing = `major non-compliant`.

##### RVU.2.2.1 Main Block Diagram
Check: is there a main block diagram?

##### RVU.2.2.2 Architecture Document
Check: is there an architecture document?

##### RVU.2.2.3 Third-Party IP List
Check: is there a list of the third-party IP used?

##### RVU.2.2.4 Logic Size/Resources/Pins Estimation and FPGA Device Selection
Check: is there a logic size, resources and pins estimation with the FPGA device selection?

#### RVU.2.3 Project Documentation
One check per project document below. Grading for each check: document present and complete = `compliant`; present but incomplete = `minor non-compliant`; missing = `major non-compliant`.

##### RVU.2.3.1 Verification Plan for Simulation
Check: has a verification plan for simulation been created?

##### RVU.2.3.2 Validation Test Plan for Lab Testing
Check: has a validation test plan document for lab testing been created?

### RVU.3 RTL Review

#### RVU.3.1 Coding Guidelines
Check the RTL code: does it follow the coding guidelines?
- Coding guidelines followed: `compliant`.
- Coding guidelines not followed: `major non-compliant`.
- Third-party coding rules took precedence over the coding guidelines: `not-applicable`.

#### RVU.3.2 Clock Distribution
Check the clock distribution: are any PLLs/DLLs chained (one PLL/DLL output feeding another PLL/DLL input)?
- No PLLs/DLLs chained: `compliant`.
- PLLs/DLLs chained: run an additional check that the chaining does not create excessive jitter outside the allowed input range of the downstream PLL/DLL.
  - Chained, and the jitter is within the allowed input range: `minor non-compliant`.
  - Chained, and the jitter is outside the allowed input range: `major non-compliant`.

#### RVU.3.3 Reset Generation and Distribution
Check the reset generation and distribution: is the initial reset deassertion driven by a proper reset generation IP or by a PLL/DLL lock signal?
- Initial reset deassertion uses a proper reset generation IP or a PLL/DLL lock signal: `compliant`.
- Initial reset deassertion does not use a proper reset generation IP or a PLL/DLL lock signal: `minor non-compliant`.

#### RVU.3.4 CDC/RDC
Check the clock domain crossings (CDC) and reset domain crossings (RDC): are they implemented with the vendor-provided IP or a pre-existing library?
- CDC/RDC uses the vendor-provided IP or a pre-existing library: `compliant`.
- CDC/RDC does not use a library: `major non-compliant`.

#### RVU.3.5 FSM Usage
Check the written RTL: is the control logic implemented with FSMs (finite state machines)?
- RTL uses FSMs: `compliant`.
- RTL does not use FSMs: `major non-compliant`.
- Exception: a simple flip-flop pipeline without an FSM: `compliant`.

#### RVU.3.6 Control Plane with SystemRDL
Check the control plane (registers): is it defined with SystemRDL?
- Control plane uses SystemRDL: `compliant`.
- Control plane does not use SystemRDL: `major non-compliant`.

### RVU.4 3rd Party Synthesis

#### RVU.4.1 MATLAB to HDL Generation
Check designs that use MATLAB: is the HDL generated directly from MATLAB, using Simulink with HDL Coder, System Generator (SysGen) or a similar tool, and are both the MATLAB/Simulink code and the generated HDL code available?
- MATLAB used together with Simulink and HDL Coder, SysGen or a similar tool to generate the HDL, and both the MATLAB/Simulink code and the generated HDL code are available: `compliant`.
- The MATLAB/Simulink code or the generated HDL code is missing: `major non-compliant`.
- MATLAB code does not generate HDL directly and the RTL was coded manually: `major non-compliant`.
- Any other tool that generates HDL directly from MATLAB counts as "similar".
- Design does not use MATLAB: `not-applicable`.

#### RVU.4.2 HLS Flow
Check designs that use HLS (high-level synthesis): are there simulation test cases in C, and are the build scripts in TCL or Python?
- HLS used, with simulation test cases in C and build scripts in TCL or Python: `compliant`.
- Anything missing: `major non-compliant`.
- Design does not use HLS: `not-applicable`.

### RVU.5 Simulation-Verification

#### RVU.5.1 Coding Guidelines
Check the verification (simulation) code: does it follow the coding guidelines?
- Coding guidelines followed: `compliant`.
- Coding guidelines not followed: `major non-compliant`.
- Third-party coding rules took precedence over the coding guidelines: `not-applicable`.

#### RVU.5.2 Simulation Methodology
Check the simulation methodology: is SIMU, or a methodology close to SSVE, used?
- SIMU or a methodology close to SSVE used: `compliant`.
- No methodology like SSVE or UVM used: `major non-compliant`.
- UVM used: `minor non-compliant`.

#### RVU.5.3 SSVE AI Project Check of the Simulation Environment
Run the SSVE AI project to check whether the simulation environment is compliant.
- No discrepancies, or only minor discrepancies found: `compliant`.
- Any other result: `major non-compliant`.

### RVU.6 PaR and STA

#### RVU.6.1 Constraints Files Organization
Check the constraints files: are they separated by type of constraint?
- Constraints files separated by type of constraint: `compliant`.
- One file with all the constraints, or a few files that are not organized: `minor non-compliant`.
- No constraints files: `major non-compliant`.

#### RVU.6.2 I/O Timing Constraints for Clocked Pins
Check the clocked signals exposed on device pins: are they constrained with input setup/hold constraints (inputs) and output "after" constraints (outputs)?
- Clocked signals on device pins have input setup/hold and output "after" constraints: `compliant`.
- Clocked signals on device pins are missing these constraints: `major non-compliant`.

### RVU.7 Lab Debug-Integration-Validation

#### RVU.7.1 Coding Guidelines
Check the validation (lab test) code: does it follow the coding guidelines?
- Coding guidelines followed: `compliant`.
- Coding guidelines not followed: `major non-compliant`.
- Third-party coding rules took precedence over the coding guidelines: `not-applicable`.

#### RVU.7.2 Python Functional Checks Against Requirement IDs
Check the validation: is Python scripting used to check the functionality against the requirement IDs?
- Python scripting checks the functionality against the requirement IDs: `compliant`.
- Otherwise: `major non-compliant`.

### RVU.8 Deliverables

#### RVU.8.1 Checklist Items in Project Output Products
Check the project output products against the checklist document (RVU.2.1.1): are all items from the checklist available?
- All checklist items are available in the project output products: `compliant`.
- Otherwise: `major non-compliant`.
