<!-- SPDX-License-Identifier: MIT -->
`SPDX-License-Identifier: MIT`

# FPGA Design Review Report: template

This template holds the main sections and subsections of the review, with a short description of the intent of each section and each line. How to carry out the review is in `claude/rules.md`, Appendix RVU Rules. The numbering here is exactly the same as in Appendix RVU Rules. Each RVU item has the review results table (rules.md rule 11) with one empty row, filled in when the review runs; RVU.0 has the scores table (Appendix RVU Rules, RVU.0), filled in last.

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
_Intent: not provided yet._

### RVU.1.1 Requirements Document
_Intent: check whether a requirements document has been used, with each requirement under a unique ID and one or two lines long._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.1.1 | | | | | |

### RVU.1.2 FPGA Project Creation TCL Scripts
_Intent: check whether FPGA project creation TCL scripts have been used._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.1.2 | | | | | |

### RVU.1.3 Simulation with SIMU
_Intent: check whether simulation has been performed with SIMU._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.1.3 | | | | | |

### RVU.1.4 Simulation/Verification Test Plan and Report
_Intent: check whether a simulation/verification test plan and a simulation/verification test report have been used._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.1.4 | | | | | |

### RVU.1.5 Validation Lab Test Plan and Report
_Intent: check whether a validation lab test plan and a validation lab test report have been used._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.1.5 | | | | | |

### RVU.1.6 Lab Testing Automation Python Scripts
_Intent: check whether lab testing automation Python scripts have been used._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.1.6 | | | | | |

### RVU.1.7 Compliance Matrix
_Intent: check for a compliance matrix linking verification and validation test cases to requirement IDs and showing the requirements not covered._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.1.7 | | | | | |

## RVU.2 Documentation
_Intent: not provided yet._

### RVU.2.1 Project Lead (PL) Documentation
_Intent: check that each required PL document exists with the required content._

#### RVU.2.1.1 Checklist Document
_Intent: check for a checklist document listing all deliverables for the project._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.2.1.1 | | | | | |

#### RVU.2.1.2 Requirements Document
_Intent: check for a requirements document listing the requirements, each under a unique ID and one or two lines long._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.2.1.2 | | | | | |

#### RVU.2.1.3 Risk Assessment
_Intent: check for a feasibility and risk assessment with mitigation strategies and two severity vs. probability risk graphs (before and after mitigation)._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.2.1.3 | | | | | |

#### RVU.2.1.4 Task List Document
_Intent: check for a task list document with effort estimates per task._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.2.1.4 | | | | | |

#### RVU.2.1.5 Change Log Document
_Intent: check for a change log, maintained throughout the project, of all changes against the initial requirements with their effort impact._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.2.1.5 | | | | | |

### RVU.2.2 Architecture Documentation
_Intent: check that each required architecture document exists._

#### RVU.2.2.1 Main Block Diagram
_Intent: check for a main block diagram._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.2.2.1 | | | | | |

#### RVU.2.2.2 Architecture Document
_Intent: check for an architecture document._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.2.2.2 | | | | | |

#### RVU.2.2.3 Third-Party IP List
_Intent: check for a list of the third-party IP used._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.2.2.3 | | | | | |

#### RVU.2.2.4 Logic Size/Resources/Pins Estimation and FPGA Device Selection
_Intent: check for a logic size, resources and pins estimation with the FPGA device selection._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.2.2.4 | | | | | |

### RVU.2.3 Project Documentation
_Intent: check that each required project document has been created._

#### RVU.2.3.1 Verification Plan for Simulation
_Intent: check that a verification plan for simulation has been created._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.2.3.1 | | | | | |

#### RVU.2.3.2 Validation Test Plan for Lab Testing
_Intent: check that a validation test plan document for lab testing has been created._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.2.3.2 | | | | | |

## RVU.3 RTL Review
_Intent: not provided yet._

### RVU.3.1 Coding Guidelines
_Intent: check that the RTL code follows the coding guidelines (not-applicable if third-party coding rules took precedence)._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.3.1 | | | | | |

### RVU.3.2 Clock Distribution
_Intent: check the clock distribution for chained PLLs/DLLs and, if chained, that the resulting jitter stays within the downstream PLL/DLL allowed input range._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.3.2 | | | | | |

### RVU.3.3 Reset Generation and Distribution
_Intent: check that the initial reset deassertion uses a proper reset generation IP or a PLL/DLL lock signal._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.3.3 | | | | | |

### RVU.3.4 CDC/RDC
_Intent: check that clock and reset domain crossings use the vendor-provided IP or a pre-existing library._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.3.4 | | | | | |

### RVU.3.5 FSM Usage
_Intent: check that the written RTL uses FSMs (simple flip-flop pipelines excepted)._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.3.5 | | | | | |

### RVU.3.6 Control Plane with SystemRDL
_Intent: check that the control plane is defined with SystemRDL._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.3.6 | | | | | |

## RVU.4 3rd Party Synthesis
_Intent: not provided yet._

### RVU.4.1 MATLAB to HDL Generation
_Intent: check that MATLAB designs generate HDL directly with Simulink and HDL Coder, SysGen or a similar tool (rather than manually coded RTL), and that both the MATLAB/Simulink code and the generated HDL code are available._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.4.1 | | | | | |

### RVU.4.2 HLS Flow
_Intent: check that HLS designs have simulation test cases in C and build scripts in TCL or Python._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.4.2 | | | | | |

## RVU.5 Simulation-Verification
_Intent: not provided yet._

### RVU.5.1 Coding Guidelines
_Intent: check that the verification (simulation) code follows the coding guidelines (not-applicable if third-party coding rules took precedence)._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.5.1 | | | | | |

### RVU.5.2 Simulation Methodology
_Intent: check that simulation uses SIMU or a methodology close to SSVE._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.5.2 | | | | | |

### RVU.5.3 SSVE AI Project Check of the Simulation Environment
_Intent: run the SSVE AI project to check whether the simulation environment is compliant._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.5.3 | | | | | |

## RVU.6 PaR and STA
_Intent: not provided yet._

### RVU.6.1 Constraints Files Organization
_Intent: check that the constraints files are separated by type of constraint._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.6.1 | | | | | |

### RVU.6.2 I/O Timing Constraints for Clocked Pins
_Intent: check that clocked signals on device pins have input setup/hold and output "after" constraints._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.6.2 | | | | | |

## RVU.7 Lab Debug-Integration-Validation
_Intent: not provided yet._

### RVU.7.1 Coding Guidelines
_Intent: check that the validation (lab test) code follows the coding guidelines (not-applicable if third-party coding rules took precedence)._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.7.1 | | | | | |

### RVU.7.2 Python Functional Checks Against Requirement IDs
_Intent: check that Python scripting is used to check the functionality against the requirement IDs._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.7.2 | | | | | |

## RVU.8 Deliverables
_Intent: not provided yet._

### RVU.8.1 Checklist Items in Project Output Products
_Intent: check that all items from the checklist document are available in the project output products._

| Item | Description | Result | Correction | Days to correct | Issue description |
|---|---|---|---|---|---|
| RVU.8.1 | | | | | |
