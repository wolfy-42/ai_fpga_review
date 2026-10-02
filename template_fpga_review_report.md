<!-- SPDX-License-Identifier: MIT -->
`SPDX-License-Identifier: MIT`

# FPGA Design Review Report: template

This template holds the main sections and subsections of the review, with a short description of the intent of each section and each line. How to carry out the review is in `claude/rules.md`, Appendix RVU Rules. The numbering here is exactly the same as in Appendix RVU Rules. Each RVU item has the review results table (rules.md rule 11) with one row: column 2 (Description) is pre-filled from Appendix RVU Rules, and columns 3–6 are filled in when the review runs; RVU.0 has the scores table (Appendix RVU Rules, RVU.0), filled in last.

---

## RVU.0 Review Scores
_Intent: the review scores are calculated after all the review sections are completed. The calculated scores are then filled in this section._

| Section ID | Section title | % compliant | % minor non-compliant | % major non-compliant |
|---|---|---|---|---|
| RVU.1 | Pre-requisites | | | |
| RVU.2 | Documentation | | | |
| RVU.3 | RTL Review | | | |
| RVU.4 | 3rd Party Synthesis | | | |
| RVU.5 | Simulation-Verification | | | |
| RVU.6 | PaR and STA | | | |
| RVU.7 | Lab Debug-Integration-Validation | | | |
| RVU.8 | Deliverables | | | |

## RVU.1 Pre-requisites

### RVU.1.1 Requirements Document
_Intent: check whether a requirements document has been used, with each requirement under a unique ID and one or two lines long._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.1.1 | Scope: checks that a requirements document is used in the project; its content is checked in RVU.2.1.2.<br>Check: has a requirements document been used, with each requirement under a unique ID and one or two lines long?<br>- Requirements document with unique requirement IDs and requirements one or two lines long used: `compliant`.<br>- A document with another structure used for the requirements (for example an architecture document): `minor non-compliant`.<br>- Neither of the above used: `major non-compliant`. | | | | |

### RVU.1.2 FPGA Project Creation TCL Scripts
_Intent: check whether FPGA project creation TCL scripts have been used._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.1.2 | Check: have FPGA project creation TCL scripts been used?<br>- TCL scripts used: `compliant`.<br>- Scripts other than TCL used: `minor non-compliant`.<br>- No project creation scripts used: `major non-compliant`. | | | | |

### RVU.1.3 Simulation with SIMU
_Intent: check whether simulation has been performed with SIMU._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.1.3 | Scope: checks the simulation flow (SIMU); the verification methodology is checked in RVU.5.2.<br>SIMU is a repo under https://github.com/wolfy-42/.<br>Check: has simulation been performed with SIMU?<br>- SIMU used: `compliant`.<br>- Simulation performed with other scripts and methodology: `minor non-compliant`.<br>- No simulation performed: `major non-compliant`. | | | | |

### RVU.1.4 Simulation/Verification Test Plan and Report
_Intent: check whether a simulation/verification test plan and a simulation/verification test report have been used._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.1.4 | Scope: checks that a simulation/verification test plan and report are used; the plan's content is checked in RVU.2.3.1.<br>Check: have a simulation/verification test plan and a simulation/verification test report been used?<br>- Simulation/verification test plan and test report used: `compliant`.<br>- Only a simulation/verification test report made, without a test plan: `minor non-compliant`.<br>- Only a simulation/verification test plan made, without a test report: `minor non-compliant`.<br>- No simulation/verification test plan and no test report: `major non-compliant`. | | | | |

### RVU.1.5 Validation Lab Test Plan and Report
_Intent: check whether a validation lab test plan and a validation lab test report have been used._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.1.5 | Scope: checks that a validation lab test plan and report are used; the plan's content is checked in RVU.2.3.2.<br>Check: have a validation lab test plan and a validation lab test report been used?<br>- Validation lab test plan and test report used: `compliant`.<br>- Only a validation lab test report made, without a test plan: `minor non-compliant`.<br>- Only a validation lab test plan made, without a test report: `minor non-compliant`.<br>- No validation lab test plan and no test report: `major non-compliant`. | | | | |

### RVU.1.6 Lab Testing Automation Python Scripts
_Intent: check whether lab testing automation Python scripts have been used._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.1.6 | Scope: checks that lab test automation is scripted in Python; what the scripts check is RVU.7.2.<br>Check: have lab testing automation Python scripts been used?<br>- Python lab testing scripts used: `compliant`.<br>- Non-Python lab testing scripts used: `minor non-compliant`.<br>- No scripting used for lab testing: `major non-compliant`. | | | | |

### RVU.1.7 Compliance Matrix
_Intent: check for a compliance matrix linking verification and validation test cases to requirement IDs and showing the requirements not covered._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.1.7 | Check: is there a compliance matrix document that links the verification test cases and the validation test cases to the requirement IDs, and shows which requirements are not covered?<br>- Compliance matrix links both verification and validation test cases to requirement IDs and shows the requirements not covered: `compliant`.<br>- Compliance matrix exists but is incomplete: `minor non-compliant`.<br>- No compliance matrix: `major non-compliant`. | | | | |

## RVU.2 Documentation

### RVU.2.1 Project Lead (PL) Documentation
_Intent: check that each required PL document exists with the required content._

#### RVU.2.1.1 Checklist Document
_Intent: check for a checklist document listing all deliverables for the project._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.2.1.1 | Check: is there a checklist document listing all deliverables for the project?<br>Grading for each check: document present and complete = `compliant`; present but incomplete = `minor non-compliant`; missing = `major non-compliant`. | | | | |

#### RVU.2.1.2 Requirements Document
_Intent: check for a requirements document listing the requirements, each under a unique ID and one or two lines long._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.2.1.2 | Scope: checks the content of the requirements document; RVU.1.1 checks that it is used.<br>Check: does the requirements document list the requirements, each under a unique ID and one or two lines long?<br>Grading for each check: document present and complete = `compliant`; present but incomplete = `minor non-compliant`; missing = `major non-compliant`. | | | | |

#### RVU.2.1.3 Risk Assessment
_Intent: check for a feasibility and risk assessment with mitigation strategies and two severity vs. probability risk graphs (before and after mitigation)._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.2.1.3 | Check: is there a risk assessment containing:<br>- a feasibility assessment, with risk assessment and mitigation strategies;<br>- two risk graphs of risk severity (low / medium / high) vs. risk probability (low / medium / high): one before mitigation, and one after mitigation is implemented.<br>Grading for each check: document present and complete = `compliant`; present but incomplete = `minor non-compliant`; missing = `major non-compliant`. | | | | |

#### RVU.2.1.4 Task List Document
_Intent: check for a task list document with effort estimates per task._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.2.1.4 | Check: is there a task list document with effort estimates per task?<br>Grading for each check: document present and complete = `compliant`; present but incomplete = `minor non-compliant`; missing = `major non-compliant`. | | | | |

#### RVU.2.1.5 Change Log Document
_Intent: check for a change log, maintained throughout the project, of all changes against the initial requirements with their effort impact._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.2.1.5 | Check: is there a change log document, maintained throughout project execution, logging all changes against the initial requirements together with their effort impact (positive or negative)?<br>Grading for each check: document present and complete = `compliant`; present but incomplete = `minor non-compliant`; missing = `major non-compliant`. | | | | |

### RVU.2.2 Architecture Documentation
_Intent: check that each required architecture document exists._

#### RVU.2.2.1 Main Block Diagram
_Intent: check for a main block diagram._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.2.2.1 | Check: is there a main block diagram?<br>Grading for each check: document present and complete = `compliant`; present but incomplete = `minor non-compliant`; missing = `major non-compliant`. | | | | |

#### RVU.2.2.2 Architecture Document
_Intent: check for an architecture document._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.2.2.2 | Check: is there an architecture document?<br>Grading for each check: document present and complete = `compliant`; present but incomplete = `minor non-compliant`; missing = `major non-compliant`. | | | | |

#### RVU.2.2.3 Third-Party IP List
_Intent: check for a list of the third-party IP used._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.2.2.3 | Check: is there a list of the third-party IP used?<br>Grading for each check: document present and complete = `compliant`; present but incomplete = `minor non-compliant`; missing = `major non-compliant`. | | | | |

#### RVU.2.2.4 Logic Size/Resources/Pins Estimation and FPGA Device Selection
_Intent: check for a logic size, resources and pins estimation with the FPGA device selection._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.2.2.4 | Check: is there a logic size, resources and pins estimation with the FPGA device selection?<br>Grading for each check: document present and complete = `compliant`; present but incomplete = `minor non-compliant`; missing = `major non-compliant`. | | | | |

### RVU.2.3 Project Documentation
_Intent: check that each required project document has been created._

#### RVU.2.3.1 Verification Plan for Simulation
_Intent: check that a verification plan for simulation has been created._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.2.3.1 | Scope: checks the content of the verification plan; RVU.1.4 checks that it is used.<br>Check: has a verification plan for simulation been created, and is it complete?<br>Grading for each check: document present and complete = `compliant`; present but incomplete = `minor non-compliant`; missing = `major non-compliant`. | | | | |

#### RVU.2.3.2 Validation Test Plan for Lab Testing
_Intent: check that a validation test plan document for lab testing has been created._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.2.3.2 | Scope: checks the content of the validation test plan; RVU.1.5 checks that it is used.<br>Check: has a validation test plan document for lab testing been created, and is it complete?<br>Grading for each check: document present and complete = `compliant`; present but incomplete = `minor non-compliant`; missing = `major non-compliant`. | | | | |

## RVU.3 RTL Review

### RVU.3.1 Coding Guidelines
_Intent: check that the RTL code follows the coding guidelines (not-applicable if third-party coding rules took precedence)._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.3.1 | Check the RTL code: does it follow the coding guidelines?<br>- Coding guidelines followed: `compliant`.<br>- Coding guidelines not followed: `major non-compliant`.<br>- Third-party coding rules took precedence over the coding guidelines: `not-applicable`. | | | | |

### RVU.3.2 Clock Distribution
_Intent: check the clock distribution for chained PLLs/DLLs and, if chained, that the resulting jitter stays within the downstream PLL/DLL allowed input range._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.3.2 | Check the clock distribution: are any PLLs/DLLs chained (one PLL/DLL output feeding another PLL/DLL input)?<br>- No PLLs/DLLs chained: `compliant`.<br>- PLLs/DLLs chained: run an additional check that the chaining does not create excessive jitter outside the allowed input range of the downstream PLL/DLL.<br>- Chained, and the jitter is within the allowed input range: `minor non-compliant`.<br>- Chained, and the jitter is outside the allowed input range: `major non-compliant`. | | | | |

### RVU.3.3 Reset Generation and Distribution
_Intent: check that the initial reset deassertion uses a proper reset generation IP or a PLL/DLL lock signal._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.3.3 | Check the reset generation and distribution: is the initial reset deassertion driven by a proper reset generation IP or by a PLL/DLL lock signal?<br>- Initial reset deassertion uses a proper reset generation IP or a PLL/DLL lock signal: `compliant`.<br>- Initial reset deassertion does not use a proper reset generation IP or a PLL/DLL lock signal: `minor non-compliant`. | | | | |

### RVU.3.4 CDC/RDC
_Intent: check that clock and reset domain crossings use the vendor-provided IP or a pre-existing library._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.3.4 | Check the clock domain crossings (CDC) and reset domain crossings (RDC): are they implemented with the vendor-provided IP or a pre-existing library?<br>- CDC/RDC uses the vendor-provided IP or a pre-existing library: `compliant`.<br>- CDC/RDC does not use a library: `major non-compliant`. | | | | |

### RVU.3.5 FSM Usage
_Intent: check that the written RTL uses FSMs (simple flip-flop pipelines excepted)._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.3.5 | Check the written RTL: is the control logic implemented with FSMs (finite state machines)?<br>- RTL uses FSMs: `compliant`.<br>- RTL does not use FSMs: `major non-compliant`.<br>- Exception: a simple flip-flop pipeline without an FSM: `compliant`. | | | | |

### RVU.3.6 Control Plane with SystemRDL
_Intent: check that the control plane is defined with SystemRDL._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.3.6 | Check the control plane (registers): is it defined with SystemRDL?<br>- Control plane uses SystemRDL: `compliant`.<br>- Control plane does not use SystemRDL: `major non-compliant`. | | | | |

## RVU.4 3rd Party Synthesis

### RVU.4.1 MATLAB to HDL Generation
_Intent: check that MATLAB designs generate HDL directly with Simulink and HDL Coder, SysGen or a similar tool (rather than manually coded RTL), and that both the MATLAB/Simulink code and the generated HDL code are available._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.4.1 | Check designs that use MATLAB: is the HDL generated directly from MATLAB, using Simulink with HDL Coder, System Generator (SysGen) or a similar tool, and are both the MATLAB/Simulink code and the generated HDL code available?<br>- MATLAB used together with Simulink and HDL Coder, SysGen or a similar tool to generate the HDL, and both the MATLAB/Simulink code and the generated HDL code are available: `compliant`.<br>- The MATLAB/Simulink code or the generated HDL code is missing: `major non-compliant`.<br>- MATLAB code does not generate HDL directly and the RTL was coded manually: `major non-compliant`.<br>- Any other tool that generates HDL directly from MATLAB counts as "similar".<br>- Design does not use MATLAB: `not-applicable`. | | | | |

### RVU.4.2 HLS Flow
_Intent: check that HLS designs have simulation test cases in C and build scripts in TCL or Python._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.4.2 | Check designs that use HLS (high-level synthesis): are there simulation test cases in C, and are the build scripts in TCL or Python?<br>- HLS used, with simulation test cases in C and build scripts in TCL or Python: `compliant`.<br>- Anything missing: `major non-compliant`.<br>- Design does not use HLS: `not-applicable`. | | | | |

## RVU.5 Simulation-Verification

### RVU.5.1 Coding Guidelines
_Intent: check that the verification (simulation) code follows the coding guidelines (not-applicable if third-party coding rules took precedence)._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.5.1 | Check the verification (simulation) code: does it follow the coding guidelines?<br>- Coding guidelines followed: `compliant`.<br>- Coding guidelines not followed: `major non-compliant`.<br>- Third-party coding rules took precedence over the coding guidelines: `not-applicable`. | | | | |

### RVU.5.2 Simulation Methodology
_Intent: check that simulation uses SIMU or a methodology close to SSVE._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.5.2 | Scope: checks the verification methodology (SIMU/SSVE-like or UVM); RVU.1.3 checks the simulation flow.<br>SIMU and SSVE are repos under https://github.com/wolfy-42/.<br>Check the simulation methodology: is SIMU, or a methodology close to SSVE, used?<br>- SIMU or a methodology close to SSVE used: `compliant`.<br>- No methodology like SSVE or UVM used: `major non-compliant`.<br>- UVM used: `minor non-compliant`. | | | | |

### RVU.5.3 SSVE AI Project Check of the Simulation Environment
_Intent: run the SSVE AI project to check whether the simulation environment is compliant._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.5.3 | Run the SSVE AI project to check whether the simulation environment is compliant.<br>- No discrepancies, or only minor discrepancies found: `compliant`.<br>- Any other result: `major non-compliant`. | | | | |

## RVU.6 PaR and STA

### RVU.6.1 Constraints Files Organization
_Intent: check that the constraints files are separated by type of constraint._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.6.1 | Check the constraints files: are they separated by type of constraint?<br>- Constraints files separated by type of constraint: `compliant`.<br>- One file with all the constraints, or a few files that are not organized: `minor non-compliant`.<br>- No constraints files: `major non-compliant`. | | | | |

### RVU.6.2 I/O Timing Constraints for Clocked Pins
_Intent: check that clocked signals on device pins have input setup/hold and output "after" constraints._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.6.2 | Check the clocked signals exposed on device pins: are they constrained with input setup/hold constraints (inputs) and output "after" constraints (outputs)?<br>- Clocked signals on device pins have input setup/hold and output "after" constraints: `compliant`.<br>- Clocked signals on device pins are missing these constraints: `major non-compliant`. | | | | |

## RVU.7 Lab Debug-Integration-Validation

### RVU.7.1 Coding Guidelines
_Intent: check that the validation (lab test) code follows the coding guidelines (not-applicable if third-party coding rules took precedence)._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.7.1 | Check the validation (lab test) code: does it follow the coding guidelines?<br>- Coding guidelines followed: `compliant`.<br>- Coding guidelines not followed: `major non-compliant`.<br>- Third-party coding rules took precedence over the coding guidelines: `not-applicable`. | | | | |

### RVU.7.2 Python Functional Checks Against Requirement IDs
_Intent: check that Python scripting is used to check the functionality against the requirement IDs._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.7.2 | Scope: checks what the Python scripts check (functionality against requirement IDs); RVU.1.6 checks the scripting language.<br>Check the validation: is Python scripting used to check the functionality against the requirement IDs?<br>- Python scripting checks the functionality against the requirement IDs: `compliant`.<br>- Otherwise: `major non-compliant`. | | | | |

## RVU.8 Deliverables

### RVU.8.1 Checklist Items in Project Output Products
_Intent: check that all items from the checklist document are available in the project output products._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.8.1 | Check the project output products against the checklist document (RVU.2.1.1): are all items from the checklist available?<br>- All checklist items are available in the project output products: `compliant`.<br>- Otherwise: `major non-compliant`. | | | | |
