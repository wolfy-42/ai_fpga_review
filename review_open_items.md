<!-- SPDX-License-Identifier: MIT -->
`SPDX-License-Identifier: MIT`

# Review Open Items: fpga review

Open items, conflicts and missing information (rules.md rules 6 and 6.1). Numbers only go up and are never reused. Closed items are removed from the list.

_Highest number used so far: 25_

**3.** **Missing:** the review rules for each Appendix RVU Rules section and subsection. RVU.0, RVU.1.1–RVU.1.7, RVU.2.1.1–RVU.2.1.5, RVU.2.2.1–RVU.2.2.4, RVU.2.3.1–RVU.2.3.2 (the RVU.2 groups are checks only, see item 16), RVU.3.1–RVU.3.5, RVU.4.1–RVU.4.2, RVU.5.1–RVU.5.2, RVU.6.1–RVU.6.2, RVU.7.1 and RVU.8.1 have their rules; still missing: any further items in RVU.1 and RVU.3–RVU.8.

**4.** **Missing:** the subsections of each review section. RVU.1 has RVU.1.1–RVU.1.7; RVU.2 has RVU.2.1 (RVU.2.1.1–RVU.2.1.5), RVU.2.2 (RVU.2.2.1–RVU.2.2.4) and RVU.2.3 (RVU.2.3.1–RVU.2.3.2); RVU.3 has RVU.3.1–RVU.3.5; RVU.4 has RVU.4.1–RVU.4.2; RVU.5 has RVU.5.1–RVU.5.2; RVU.6 has RVU.6.1–RVU.6.2; RVU.7 has RVU.7.1; RVU.8 has RVU.8.1; RVU.0 has none defined yet.

**6.** **Missing:** the first design to review.

**7.** **Missing:** the intent descriptions for each section and line of `template_fpga_review_report.md`. RVU.0, RVU.1.1–RVU.1.7, RVU.2.1–RVU.2.3 (with all their sub-items), RVU.3.1–RVU.3.5, RVU.4.1–RVU.4.2, RVU.5.1–RVU.5.2, RVU.6.1–RVU.6.2, RVU.7.1 and RVU.8.1 have been provided; RVU.1, RVU.2, RVU.3, RVU.4, RVU.5, RVU.6, RVU.7 and RVU.8 are still missing.

**8.** **Missing:** where `fpga_review_report.md` is stored and how it is named when there is more than one design review (rule 8.2 / 8.3).

**11.** **Conflict:** D's instruction for rule 11 said the review results table has 4 columns, but then defined 6 columns. Rule 11 currently lists all 6. Needs D to confirm 6 columns.

**12.** **Missing:** whether `template_fpga_review_report.md` should be changed to include the rule 11 table (empty, with the 6 column headers) under each section, so `fpga_review_report.md` starts with it (rule 8.3).

**13.** **Missing:** a definition of SIMU (RVU.1.3): what it is and how a reviewer recognizes that a design used it (for example a link to it, or the files or structure it produces).

**14.** **Missing:** the grading for RVU.1.4 and RVU.1.5 when a test plan exists but there is no test report. Each rule only covers plan + report, report only, and neither.

**15.** **Missing:** whether items graded `not-applicable` count in a section's total items for the RVU.0 percentages. If they count, the three percentages won't add up to 100% when a section has not-applicable items.

**16.** **Missing:** the grading (compliant / minor non-compliant / major non-compliant) for RVU.2.1.1–RVU.2.1.5, RVU.2.2.1–RVU.2.2.4 and RVU.2.3.1–RVU.2.3.2, for example when a document is missing versus present but incomplete.

**17.** **Conflict:** RVU.1.1 describes the requirements document as "short one-line requirements" with unique IDs, while RVU.2.1.2 describes it as requirements under unique IDs with "a couple of lines of description" each. Needs D to confirm whether these are the same document and which format is expected (for example a one-line requirement plus a short description).

**19.** **Missing:** RVU.3.1 Clock Distribution grading details: (a) the grade when no PLLs/DLLs are chained (for example `compliant`); (b) whether chained PLLs/DLLs stay `major non-compliant` even when the additional jitter check passes, and what grade applies if the jitter is outside the downstream PLL/DLL allowed input range.

**20.** **Missing:** RVU.3.2 Reset Generation and Distribution grading when the initial reset deassertion does not use a proper reset generation IP or a PLL/DLL lock signal (minor or major non-compliant), and whether anything else about reset distribution should be checked.

**21.** **Missing:** RVU.3.4 FSM Usage: the grade for logic that is a simple flip-flop pipeline without an FSM (`compliant` or `not-applicable`).

**22.** **Missing:** RVU.6.1 Constraints Files Organization: the grade when there are no constraints files at all (for example `major non-compliant`), and which constraint types are expected as separate files (for example timing, pins/IO, placement).

**23.** **Missing:** RVU.5.1 Simulation Methodology: (a) what SSVE stands for and where it is defined; (b) the grade when UVM (or another established methodology that is not SSVE-like) is used — the rule only says SIMU/SSVE-like = compliant and no methodology like SSVE or UVM = major non-compliant; (c) whether RVU.5.1 overlaps RVU.1.3 Simulation with SIMU.

**24.** **Missing:** RVU.5.2 SSVE AI Project Check: (a) where the SSVE AI project is and how to run it; (b) what counts as a "minor" vs. other discrepancy; (c) confirm the grading — as written, minor discrepancies are `compliant` (not `minor non-compliant`).

**25.** **Missing:** RVU.4.1 MATLAB to HDL Generation and RVU.4.2 HLS Flow: (a) the grade when the design does not use MATLAB (RVU.4.1) or HLS (RVU.4.2) at all (for example `not-applicable`); (b) for RVU.4.1, the grade when MATLAB generates HDL some other way (not Simulink + HDL Coder or SysGen), if that counts as "similar".
