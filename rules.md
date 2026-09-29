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

**4.** **Review-section rules go in Appendix R.** Rules for reviewing a specific section of a review go in Appendix R, numbered to match the review: R.N covers review section R.N, and R.N.M covers subsection R.N.M (and so on for deeper levels). When reviewing a section, apply every rule under its R.N entry, including those in its subsections.

**5.** **Hierarchical numbering.** Everything in the project is numbered hierarchically: 1., 1.1, 1.1.1 and so on, going as deep as needed. This covers rules, review sections, appendix entries and any other numbered lists. Appendices use the same scheme with a letter prefix: R.1, R.1.1, R.1.1.1.

**6.** **Track open items in `review_open_items.md`.** Store every open item, conflict and piece of missing information in `claude/review_open_items.md` as a numbered list.

**6.1** **Open-item numbers only go up and are never reused.** Number open items in sequence, always taking the next number after the highest one ever used. When an item is closed, remove it from the list, but never give its number to another item.

**7.** **Never assume, never fill in content.** Use only information D has given. Don't generate, infer or fill in content from general knowledge or assumptions. If something needed is missing or unclear, leave it empty and log it as an open item under rule 6.

**8.** **Run the review in Appendix R order, one line at a time.** Run the review following the sequence of the sections and subpoints in Appendix R.

**8.1** Every line in Appendix R is a separate execution of the rule written on that line.

**8.2** Capture the result of each execution in `fpga_review_report.md`, in the matching section or subpoint.

**8.3** `fpga_review_report.md` starts as a copy of `template_fpga_review_report.md`, which gives it its original structure.

**9.** **The template mirrors Appendix R.** `template_fpga_review_report.md` is a copy of the sections in Appendix R, with exactly the same numbering (R.0, R.1, R.1.1 …). Any discrepancy between the two is flagged as a conflict in `review_open_items.md` (rule 6).

**10.** **"help" / "menu" command.** When D types `help` or `menu`, list the example command prompts below.

**10.1** `execute review`: runs the full review (rule 8).

**10.2** `execute review of section R.3`: runs the review of section R.3 only. Any section number can be used, for example R.N or R.N.M.

---

## Appendix R: Review-section rules

Rules for reviewing each section of the review, numbered to match it: R.N covers review section R.N, and R.N.M covers subsection R.N.M.

### R.0 Review Scores
_No rules yet._

### R.1 Pre-requisites
_No rules yet._

### R.2 TPL Documentation
_No rules yet._

### R.3 Architecture Documentation
_No rules yet._

### R.4 RTL Review
_No rules yet._

### R.5 3rd Party Synthesis
_No rules yet._

### R.6 Simulation-Verification
_No rules yet._

### R.7 PaR and STA
_No rules yet._

### R.8 Lab Debug-Integration-Validation
_No rules yet._

### R.9 Deliverables
_No rules yet._
