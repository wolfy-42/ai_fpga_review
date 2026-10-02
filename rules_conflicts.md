<!-- SPDX-License-Identifier: MIT -->
`SPDX-License-Identifier: MIT`

# Rules Conflicts and Open Items: fpga review

Conflicts, missing information and open items about the project rules: `rules.md` (including Appendix RVU Rules) and `template_fpga_review_report.md` (rules.md rule 13). Items are numbered OI.1, OI.2 … with sub-items OI.N.M. Numbers only go up and are never reused. Closed items are removed from the list.

Open items about the design under review go in `review_open_items.md` instead (rule 6).

_Highest number used so far: OI.12_

**OI.4** **Missing:** SIMU (RVU.1.3, RVU.5.2). Known: SIMU is a repo under https://github.com/wolfy-42/. Still needed: the exact repo link, and how a reviewer recognizes that a design used it (for example the files or folder structure it produces).

**OI.5** **Missing:** RVU.5.2 Simulation Methodology.

**OI.5.1** What SSVE stands for, and the exact repo link (known: SSVE is a repo under https://github.com/wolfy-42/).

**OI.6** **Missing:** RVU.5.3 SSVE AI Project Check.

**OI.6.1** Where the SSVE AI project is (a repo under https://github.com/wolfy-42/?) and how to run it.

**OI.6.2** What counts as a "minor" discrepancy vs. any other discrepancy.

**OI.12** **Missing:** the coding guidelines used by RVU.3.1 (RTL), RVU.5.1 (verification) and RVU.7.1 (validation): where they are and which version applies, and how a reviewer tells that third-party coding rules took precedence (for example, stated in the project documents).
