<!-- SPDX-License-Identifier: MIT -->
`SPDX-License-Identifier: MIT`

# Review Open Items: fpga review

Open items, conflicts and missing information (rules.md rules 6 and 6.1). Numbers only go up and are never reused. Closed items are removed from the list.

_Highest number used so far: 31_

**3.** **Missing:** the review rules for each Appendix RVU Rules section and subsection. Every major section RVU.1–RVU.8 now has at least one rule; still open: any further items D wants to add.

**4.** **Missing:** the subsections of each review section. RVU.1 has RVU.1.1–RVU.1.7; RVU.2 has RVU.2.1 (RVU.2.1.1–RVU.2.1.5), RVU.2.2 (RVU.2.2.1–RVU.2.2.4) and RVU.2.3 (RVU.2.3.1–RVU.2.3.2); RVU.3 has RVU.3.1–RVU.3.6; RVU.4 has RVU.4.1–RVU.4.2; RVU.5 has RVU.5.1–RVU.5.3; RVU.6 has RVU.6.1–RVU.6.2; RVU.7 has RVU.7.1–RVU.7.2; RVU.8 has RVU.8.1. Still open: any further subsections D wants to add.

**6.** **Missing:** the first design to review.

**7.** **Missing:** the intent descriptions for the major sections in `template_fpga_review_report.md`: RVU.1–RVU.8 still say "not provided yet" (every sub-item already has one).

**13.** **Missing:** a definition of SIMU (RVU.1.3, RVU.5.2): what it is and how a reviewer recognizes that a design used it (for example a link to it, or the files or structure it produces).

**23.** **Missing:** RVU.5.2 Simulation Methodology: (a) what SSVE stands for and where it is defined; (b) whether RVU.5.2 overlaps RVU.1.3 Simulation with SIMU, and if so whether both checks should stay.

**24.** **Missing:** RVU.5.3 SSVE AI Project Check: (a) where the SSVE AI project is and how to run it; (b) what counts as a "minor" discrepancy vs. any other discrepancy.

**26.** **Missing:** where the Excel copy of the review report (rule 12) is stored. Project docs hold text files, so the `.xlsx` may not be storable in `claude/reviews/`; possible places are the Mac repo folder next to the `.md`, or delivered as a download in the chat.

**27.** **Conflict (duplicate checks):** some items check the same thing twice, so one gap would count against two sections in RVU.0: (a) the requirements document in RVU.1.1 and RVU.2.1.2; (b) the simulation test/verification plan in RVU.1.4 and RVU.2.3.1; (c) the validation lab test plan in RVU.1.5 and RVU.2.3.2; (d) Python lab scripts in RVU.1.6 and Python functional checks against requirement IDs in RVU.7.2; (e) SIMU use in RVU.1.3 and RVU.5.2 (also item 23). Needs D to decide: keep both, or keep one and drop or reword the other.

**28.** **Missing:** results table columns 4 and 5 (rule 11.4, 11.5): who decides whether an item will be corrected or left uncorrected, and who gives the days to correct (the reviewer, or the design team)? And the allowed values for column 4 (for example `to be corrected` / `left uncorrected`), and whether columns 4–6 stay empty for `compliant` and `not-applicable` items.

**29.** **Missing:** RVU.0 percentages when every item in a section is `not-applicable` (for example RVU.4 when the design uses neither MATLAB nor HLS): show `N/A` in the row, or leave the row out?

**30.** **Missing:** whether the template's column 2 (Description) should be pre-filled from Appendix RVU Rules (the check and its grading), so the reviewer only fills columns 3–6; or left empty and filled during the review.

**31.** **Missing:** the coding guidelines used by RVU.3.1 (RTL), RVU.5.1 (verification) and RVU.7.1 (validation): where they are and which version applies, and how a reviewer tells that third-party coding rules took precedence (for example, stated in the project documents).
