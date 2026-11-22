# Software Requirements Specification for FixMyRoom

**Course:** Requirements Engineering (INCS508)  
**Semester:** Winter 2026  
**Milestone:** 1  
**Prepared by:** Team AMOSA  
**Version:** 0.1 — Draft  
**Date:** [Enter date]

## Table of Contents

1. [Introduction](#1-introduction)
2. [Overall Description](#2-overall-description)
3. [External Interface Requirements](#3-external-interface-requirements)
4. [System Features](#4-system-features)
5. [Other Nonfunctional Requirements](#5-other-nonfunctional-requirements)
6. [Other Requirements](#6-other-requirements)
7. [Appendix A — Glossary](#appendix-a--glossary)
8. [Appendix B — Analysis Models](#appendix-b--analysis-models)
9. [Appendix C — To Be Determined List](#appendix-c--to-be-determined-list)

## Revision History

| Name | Date | Reason for change | Version |
| --- | --- | --- | --- |
| [Author] | [Date] | Created the shared SRS outline | 0.1 |

## 1. Introduction

### 1.1 Purpose

[Identify the product and explain what this SRS specifies for Milestone 1.]

### 1.2 Document Conventions

[Explain the feature IDs F1–F5, requirement IDs R01–R15, and classifications FR, NFR, and C. Define the priority scale used in Section 4.]

### 1.3 Intended Audience and Reading Suggestions

[Identify who will read the SRS and which sections are most relevant to each audience.]

### 1.4 Product Scope

[Summarize the client’s problem, the goals of FixMyRoom, and the boundaries of this version.]

### 1.5 References

[List the FixMyRoom case description, Milestone 1 brief, and other sources the team actually uses.]

## 2. Overall Description

### 2.1 Product Perspective

[Explain how maintenance requests are handled today and where FixMyRoom fits into that process.]

### 2.2 Product Functions

[Give a short overview of F1–F5 and how they work together. Refer to Section 4 for the details.]

### 2.3 User Classes and Characteristics

[Identify the people who will directly use this version and what each needs to do. Distinguish users from other interested stakeholders.]

### 2.4 Operating Environment

[Describe where and on what devices or software the system is expected to run.]

### 2.5 Design and Implementation Constraints

[Record relevant limits from the case or agreed project decisions. Identify the source of each.]

### 2.6 User Documentation

[Identify the instructions that will accompany the prototype and where the reader can find them.]

### 2.7 Assumptions and Dependencies

[Record assumptions the team made about details left open in the case. Identify anything the system depends on.]

## 3. External Interface Requirements

### 3.1 User Interfaces

[Describe the main user-facing screens and which user classes interact with each.]

### 3.2 Hardware Interfaces

[Describe any direct hardware interfaces that apply to this version.]

### 3.3 Software Interfaces

[Identify any software systems or services that FixMyRoom exchanges information with.]

### 3.4 Communications Interfaces

[Describe the communication mechanisms the agreed system depends on, where applicable.]

## 4. System Features

<!-- Editing guide for the five feature owners:
Type = FR (functional), NFR (non-functional), or C (constraint).
Case source = a specific case section, business goal, or stakeholder need.
If a detail is a team decision, identify it as an assumption or decision.
Prototype check = the action a reviewer takes and the result they should observe.
Define each requirement once. Refer to its ID elsewhere in the SRS.
Remove this editing guide before submission. -->

### 4.1 F1 — Maintenance Request Reporting

#### 4.1.1 Description and Priority

Residents use FixMyRoom to report faults in their rooms or in shared areas. Each new request has a reference the resident can use to find it again. If another resident has already reported the same shared-area fault, a resident can follow that request using its existing reference.

**Priority — High.** CampusLiving currently loses reports and receives several reports about the same fault. Caretakers need a saved request with a clear location before they can assign a repair.

#### 4.1.2 Stimulus/Response Sequences

| User action or event | Expected system response |
| --- | --- |
| A resident enters the building, room or shared-area location, and fault description, then submits the report. | FixMyRoom saves the request and its submission time, then shows the resident its reference and initial status, **Received**. |
| After an application restart, the resident opens the confirmed request using its reference. | FixMyRoom displays the saved location and fault description under the original reference. |
| A second resident selects the same shared area while reporting a fault. | FixMyRoom shows open requests for that shared area so the resident can identify whether the fault has already been reported. |
| The second resident selects the matching request and chooses **Follow**. | FixMyRoom adds the resident as a follower of the existing request. The reference and the number of maintenance requests stay the same. |

#### 4.1.3 Requirements

| ID | Type | Requirement statement | Case source | Prototype check |
| --- | --- | --- | --- | --- |
| R01 | FR | When a resident submits a building, a room or shared-area location, and a fault description, FixMyRoom shall create one request with those details and its submission time, and confirm it with a unique reference and the status **Received**. | FixMyRoom case, p. 1, *Problem*, and p. 2, BG1 and BG4. The reference and initial status are team decisions. | Submit a private-room fault and a separate shared-area fault. Verify that each submission produces one request with the entered details, a submission time, a distinct reference, and the status **Received**. |
| R02 | NFR | After FixMyRoom confirms a submission, the request shall remain retrievable by its original reference after the application restarts, with its submitted details and submission time preserved. | FixMyRoom case, p. 2, BG1. Surviving an application restart is the team's reliability criterion. | Record a confirmed request's reference, details, and submission time. Restart the application and retrieve the request as the same resident. Compare the saved values with the originals. |
| R03 | FR | When a resident selects an open request for the same shared-area fault and chooses to follow it, FixMyRoom shall link that resident to the selected request without creating a second maintenance request. | FixMyRoom case, p. 1, *Problem*, and p. 3, *First Questions to Think About*, question 4. Following an existing request is the team's chosen response to duplicate reports. | Have one resident report a shared-kitchen fault. As a second resident, select that fault and follow it. Verify that both residents can access the same reference and that the total request count remains unchanged. |

### 4.2 F2 — Work Prioritization and Scheduling

#### 4.2.1 Description and Priority

**Description:** [Describe F2 and the need it addresses.]  
**Priority and rationale:** [State the priority and explain why.]

#### 4.2.2 Stimulus/Response Sequences

| User action or event | Expected system response |
| --- | --- |
| [Action or event] | [Observable response] |

#### 4.2.3 Requirements

| ID | Type | Requirement statement | Case source | Prototype check |
| --- | --- | --- | --- | --- |
| R04 | | | | |
| R05 | | | | |
| R06 | | | | |

### 4.3 F3 — Repair Progress Tracking

#### 4.3.1 Description and Priority

**Description:** [Describe F3 and the need it addresses.]  
**Priority and rationale:** [State the priority and explain why.]

#### 4.3.2 Stimulus/Response Sequences

| User action or event | Expected system response |
| --- | --- |
| [Action or event] | [Observable response] |

#### 4.3.3 Requirements

| ID | Type | Requirement statement | Case source | Prototype check |
| --- | --- | --- | --- | --- |
| R07 | | | | |
| R08 | | | | |
| R09 | | | | |

### 4.4 F4 — Repair Confirmation and Closure

#### 4.4.1 Description and Priority

**Description:** [Describe F4 and the need it addresses.]  
**Priority and rationale:** [State the priority and explain why.]

#### 4.4.2 Stimulus/Response Sequences

| User action or event | Expected system response |
| --- | --- |
| [Action or event] | [Observable response] |

#### 4.4.3 Requirements

| ID | Type | Requirement statement | Case source | Prototype check |
| --- | --- | --- | --- | --- |
| R10 | | | | |
| R11 | | | | |
| R12 | | | | |

### 4.5 F5 — Maintenance Performance Reporting

#### 4.5.1 Description and Priority

**Description:** [Describe F5 and the need it addresses.]  
**Priority and rationale:** [State the priority and explain why.]

#### 4.5.2 Stimulus/Response Sequences

| User action or event | Expected system response |
| --- | --- |
| [Action or event] | [Observable response] |

#### 4.5.3 Requirements

| ID | Type | Requirement statement | Case source | Prototype check |
| --- | --- | --- | --- | --- |
| R13 | | | | |
| R14 | | | | |
| R15 | | | | |

## 5. Other Nonfunctional Requirements

### 5.1 Performance Requirements

[Reference any applicable requirement IDs and explain how performance will be assessed.]

### 5.2 Safety Requirements

[Document applicable safety considerations and reference the requirements they affect.]

### 5.3 Security Requirements

[Reference requirements that address access to information, privacy, or permissions.]

### 5.4 Software Quality Attributes

[Reference relevant quality requirements, such as reliability or usability, and their verification methods.]

### 5.5 Business Rules

[Record the agreed business rules that apply across features. Refer to existing requirement IDs where appropriate.]

## 6. Other Requirements

[Document any remaining applicable considerations. Keep the milestone total at 15 uniquely identified requirements.]

## Appendix A — Glossary

| Term | Meaning in FixMyRoom |
| --- | --- |
| [Term] | [Agreed definition] |

## Appendix B — Analysis Models

[Include or link any models the team uses to explain the system, such as an agreed request-status diagram.]

## Appendix C — To Be Determined List

| Open question | Affected feature or section | Owner | Status or decision |
| --- | --- | --- | --- |
| [Question] | [Feature ID or section] | [Team member] | [Open or resolved] |