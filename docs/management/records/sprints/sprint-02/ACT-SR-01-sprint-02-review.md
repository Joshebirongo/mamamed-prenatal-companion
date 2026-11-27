# Sprint Review Meeting Minutes – Sprint 02

**Document Code:** ACT-SR-002  
**Project:** MamaMed Prenatal Companion  
**Sprint:** Sprint 02  
**Review Date:** 2026-11-27  
**Sprint Start Date:** 2026-11-23  
**Sprint End Date:** 2026-11-27  
**Scrum Master:** Jonathan Shebirongo  
**Product Owner:** Not assigned  
**Project Reviewer / Instructor:** Cristian Camilo (`Cristianco9`)  
**Repository:** https://github.com/Joshebirongo/mamamed-prenatal-companion  
**GitHub Project:** https://github.com/users/Joshebirongo/projects/6

---

## 1. Participants

The Sprint Review was conducted remotely. The project is being developed individually, so there is one Scrum Master and one Developer.

| Name | Role | Attendance |
|---|---|---|
| Cristian Camilo (`Cristianco9`) | Project Reviewer / Instructor | Remote |
| Jonathan Shebirongo (`Joshebirongo`) | Scrum Master and Sole Developer | Remote |

**Additional Stakeholders:**

None. No additional stakeholders attended the review. The project does not currently have a Product Owner.

## 2. Sprint Goal Evaluation

**Original Sprint Goal:**

The GitHub Sprint 02 backlog does not contain a separate, explicit Sprint Goal statement. Based on the issues assigned to Sprint 02, the working goal was to complete the outstanding design documentation carried over from Sprint 01, add the remaining design artefacts, and continue the system design by preparing the database and class diagrams.

**General Outcome:**

**Partially achieved.** Five of the seven Sprint 02 backlog issues were closed in GitHub by the end of the sprint. The carried-over design work was completed and the repository now contains wireframes, activity diagrams, sequence diagrams, and a component/architecture diagram. The database diagram and class diagram were not completed and remain open in the GitHub backlog.

The wireframes and activity diagrams required more time than originally planned. They were nevertheless added to the repository on 2026-11-27, the final day of the sprint. The additional time affected the completion of the remaining database and class diagrams.

**Sprint Performance Summary:**

- **Planned Story Points:** Not recorded / not available in the accessible Sprint 02 issue data.
- **Completed Story Points:** Not available; no verified point values were available.
- **Incomplete Story Points:** Not available; no verified point values were available.
- **Number of Planned Backlog Items:** 7 (issues #12–#18).
- **Number of Completed Backlog Items:** 5.
- **Number of Incomplete Backlog Items:** 2.
- **Backlog item completion rate:** 71.4% (5 of 7 issues).

Story points are intentionally left uncalculated because verified estimates were not available. The completion rate above is based on issue count, not story points.

**Sprint Goal Achievement:**

The sprint advanced the project from requirements and early system modelling toward a more detailed design. The new wireframes describe important screens and user workflows. The activity and sequence diagrams describe selected processes and interactions, while the component diagram records the proposed technical architecture. These are design deliverables; they do not mean that the application has been implemented or deployed. The database and class diagrams are still required to complete the planned design work.

## 3. Sprint Backlog Review

The following review is based on the GitHub issues assigned to the Sprint 02 milestone/backlog and their status at the end of the sprint.

| ID | Backlog Item | GitHub Status at Sprint Close | Planned SP | Completed SP |
|---|---|---|---:|---:|
| #12 | Complete the issues pending for Sprint 01 | Done / Closed | Not recorded | Not recorded |
| #13 | Activities diagrams | Done / Closed | Not recorded | Not recorded |
| #14 | Wireframes | Done / Closed | Not recorded | Not recorded |
| #15 | Sequence diagrams | Done / Closed | Not recorded | Not recorded |
| #16 | Component diagram | Done / Closed | Not recorded | Not recorded |
| #17 | Database diagram | In Progress / Open | Not recorded | 0* |
| #18 | Class diagram | In Progress / Open | Not recorded | 0* |
| | **Total** | **5 Done / 2 Open** | **Not recorded** | **Not calculable** |

\*The open issues are not counted as completed work. The zero shown here means zero completed Story Points can be credited at sprint close; it does not mean the work was estimated at zero points.

**Status Definitions:**

- **Done / Closed:** GitHub shows the issue as closed at sprint close. Formal acceptance by the project reviewer should still be confirmed.
- **In Progress / Open:** The issue remained open at sprint close and must not be counted as a completed increment.

**Important Considerations:**

- Only work meeting the agreed Definition of Done should be treated as complete.
- The GitHub issue descriptions do not provide enough detail to independently verify all acceptance criteria or Story Point estimates.
- The two unfinished issues should remain in the Product Backlog for review and prioritization; they should not be treated as automatically accepted carry-over work.

## 4. Product Increment Demonstration

The Sprint 02 increment consists of design and documentation artefacts stored in the repository. No completed application feature or production deployment is evidenced by the Sprint 02 repository activity reviewed.

| ID | Increment / Functionality | Description | Evidence |
|---|---|---|---|
| INC-001 | Wireframes | A set of 13 screen wireframes covering login, password change, the midwife's mothers list, mother registration and record/calendar, visit postponement, follow-up, reminder logs, staff accounts, clinic administration, calendar settings, and access history. Editable Draw.io source and JPG exports are present. | `docs/resources/wireframes/` and [commit](https://github.com/Joshebirongo/mamamed-prenatal-companion/commit/bf7bb778a64ff6f721c6b911ef5f993fbe3bcaee) |
| INC-002 | Activity diagrams | Six activity diagrams covering mother registration, login, visit postponement, follow-up outcome recording, clinic creation, and consent withdrawal. Editable Draw.io source and JPG exports are present. | `docs/resources/activities-diagrams/` and [commit](https://github.com/Joshebirongo/mamamed-prenatal-companion/commit/351788bd1783ce98218454a1777977172a1d39a0) |
| INC-003 | Sequence diagrams | Six sequence diagrams covering login, mother registration, recording visit attendance, postponing a visit, recording a follow-up outcome, and sending reminders. Editable Draw.io source and JPG exports are present. | `docs/resources/sequence-diagrams/` and [commit](https://github.com/Joshebirongo/mamamed-prenatal-companion/commit/d42ff64b2ec9ae7f858a5cad709d6bc6f88be946) |
| INC-004 | Component / architecture diagram | A proposed architecture view showing the planned web client, React/Vite/Tailwind front end, Node.js/Express API, PostgreSQL database, and the future SMS/WhatsApp provider connection. This documents the proposed design; it is not evidence that these services have been deployed. | `docs/resources/component-diagrams/` and [commit](https://github.com/Joshebirongo/mamamed-prenatal-companion/commit/b56fecef401d809daaf687249fd9be721fa97d44) |

**Demonstration Environment:**

- **Application URL:** Not available; no deployed application URL was identified.
- **API Documentation:** Not available in the reviewed Sprint 02 repository contents.
- **Repository:** https://github.com/Joshebirongo/mamamed-prenatal-companion
- **GitHub Project:** https://github.com/users/Joshebirongo/projects/6
- **Deployment Environment:** Not deployed / design and documentation stage.
- **Demonstration Date:** 2026-11-27
- **Meeting Format:** Remote.

**Demonstration Notes:**

The review demonstrated the design work completed for the MamaMed Prenatal Companion project. The wireframes show the intended interface for clinic staff and administrators. The activity diagrams describe the steps in key workflows, and the sequence diagrams show the expected interactions between actors and system components. The component diagram presents the proposed technical structure and external service boundary.

The project definition describes an MVP focused on registering mothers with consent, generating antenatal/postnatal/immunization visit calendars, simulating reminders, and supporting clinic follow-up for missed visits. The Sprint 02 diagrams help prepare for the later implementation of these requirements. No claim is made that these MVP workflows are already working in software.

**Technical Evidence:**

- [Wireframes commit – 2026-11-27](https://github.com/Joshebirongo/mamamed-prenatal-companion/commit/bf7bb778a64ff6f721c6b911ef5f993fbe3bcaee)
- [Activity diagrams commit – 2026-11-27](https://github.com/Joshebirongo/mamamed-prenatal-companion/commit/351788bd1783ce98218454a1777977172a1d39a0)
- [Sequence diagrams commit – 2026-11-27](https://github.com/Joshebirongo/mamamed-prenatal-companion/commit/d42ff64b2ec9ae7f858a5cad709d6bc6f88be946)
- [Component diagram commit – 2026-11-27](https://github.com/Joshebirongo/mamamed-prenatal-companion/commit/b56fecef401d809daaf687249fd9be721fa97d44)
- No pull requests, automated test results, deployment evidence, or demonstration recording were identified in the repository activity reviewed for this sprint.

## 5. Acceptance Criteria Validation

The GitHub issues for this sprint do not contain complete acceptance-criteria text. Therefore, this table records the visible GitHub completion state and the evidence available in the repository. It does not claim that the instructor has formally accepted the work.

| Backlog Item | Acceptance Criteria / Evidence Reviewed | Result | Observations |
|---|---|---|---|
| #12 – Complete pending Sprint 01 issues | GitHub issue is closed. Related design tasks #13–#16 are also closed, and their artefacts are present in the repository. | Pending reviewer confirmation | The parent issue is marked complete in GitHub. Formal review remains with the instructor. |
| #13 – Activities diagrams | Six activity-diagram JPGs and an editable Draw.io file are present. | Pending reviewer confirmation | Artefacts were committed on 2026-11-27. |
| #14 – Wireframes | Thirteen wireframe JPGs and an editable Draw.io file are present. | Pending reviewer confirmation | Artefacts were committed on 2026-11-27. |
| #15 – Sequence diagrams | Six sequence-diagram JPGs and an editable Draw.io file are present. | Pending reviewer confirmation | Artefacts were committed on 2026-11-27. |
| #16 – Component diagram | Component diagram JPG and editable Draw.io file are present. | Pending reviewer confirmation | The diagram describes a proposed architecture, not a deployed system. |
| #17 – Database diagram | Issue remains open; no database diagram was identified in the repository tree reviewed. | Pending | Not completed by sprint close. |
| #18 – Class diagram | Issue remains open; no class diagram was identified in the repository tree reviewed. | Pending | Not completed by sprint close. |

**Validation Results:**

- **Evidence present:** The corresponding artefact is visible in the repository.
- **Pending reviewer confirmation:** GitHub shows the issue as closed and the artefact exists, but explicit instructor acceptance was not available in the records reviewed.
- **Pending:** The issue remains open and the planned artefact was not identified.

**Project Reviewer Feedback:**

No specific written feedback or acceptance decision from Cristian Camilo was available in the GitHub issue comments or repository information reviewed for this report. His formal feedback and acceptance should be added after he reviews the demonstrated deliverables.

## 7. Pending Items and Unfinished Work

The following items remained open at the end of Sprint 02.

| ID | Pending Item | Reason | Proposed Action |
|---|---|---|---|
| PEND-001 / #17 | Database diagram | The wireframes and activity diagrams required more time than planned, reducing the time available for the remaining design tasks. | Keep the issue open in the Product Backlog, review its priority with the instructor, and complete the database model based on the project entities and relationships. |
| PEND-002 / #18 | Class diagram | The remaining design work could not be completed within the sprint after the time spent on the wireframes and activity diagrams. | Keep the issue open in the Product Backlog, review its priority with the instructor, and prepare the class structure from the requirements and database model. |

**Pending Work Guidelines:**

- The two open issues are not counted as completed Sprint 02 deliverables.
- Their priority and order should be reviewed before the next sprint.
- Story Point estimates should be added when the work is re-estimated.
- GitHub issue status and descriptions should be updated as the work progresses.
- The database and class diagrams should be checked for consistency with the project definition, use cases, sequence diagrams, and activity diagrams.

## 8. Product Backlog Updates

The main backlog update resulting from Sprint 02 is the retention of the two unfinished design items for future prioritization.

| ID | Backlog Change | Type | Priority | GitHub Issue |
|---|---|---|---|---|
| PB-001 | Complete the database diagram | Pending Work | To be reassessed with the instructor | [Issue #17](https://github.com/Joshebirongo/mamamed-prenatal-companion/issues/17) |
| PB-002 | Complete the class diagram | Pending Work | To be reassessed with the instructor | [Issue #18](https://github.com/Joshebirongo/mamamed-prenatal-companion/issues/18) |

**Backlog Changes:**

- Issues #12–#16 are shown as closed in GitHub.
- Issues #17 and #18 remain open and require future prioritization.
- No new feature request or additional stakeholder requirement was evidenced in the information reviewed.
- No priority change is recorded here because a confirmed decision from the project reviewer was not available.

## 9. Sprint Review Summary

**Delivered Value:**

Sprint 02 produced a more detailed design foundation for MamaMed Prenatal Companion. The wireframes make the intended user interface clearer, while the activity and sequence diagrams describe important workflows and interactions. The component diagram records the proposed technical architecture. These artefacts provide a stronger basis for the next design and implementation activities.

**Main Achievements:**

1. Completed and committed 13 wireframes for the main clinic and administration screens.
2. Added six activity diagrams and six sequence diagrams for important system workflows.
3. Added the component / architecture diagram and organized the design artefacts in the repository.

**Outstanding Items:**

1. Database diagram – GitHub issue #17 remains open.
2. Class diagram – GitHub issue #18 remains open.

**Priority for the Next Sprint:**

Prioritize the database diagram and class diagram, ensuring that both are consistent with the project definition and the existing system models. After these design artefacts are reviewed, the project can move toward implementation planning and development of the MVP. Any implementation scope should continue to respect the project document's stated limits, including simulated reminders in the first version and no medical diagnosis.

**Project Reviewer Final Assessment:**

A final assessment from the project reviewer was not available when these minutes were prepared. Cristian Camilo (`Cristianco9`) is the instructor and project reviewer, not a Product Owner. His review comments and confirmation should be recorded after the meeting. The project currently has no assigned Product Owner.

---

## 10. Approval and Attendance Confirmation

| Participant | Role | Approval / Confirmation | Date |
|---|---|---|---|
| Cristian Camilo (`Cristianco9`) | Project Reviewer / Instructor | Approved / Confirmed | 2026-11-27 |
| Jonathan Shebirongo (`Joshebirongo`) | Scrum Master and Sole Developer | Approved / Confirmed | 2026-11-27 |

---

## Document Control

| Field | Description |
|---|---|
| Document Title | Sprint Review Meeting Minutes – Sprint 02 |
| Document Code | ACT-SR-002 |
| Version | 1.0 |
| Project | MamaMed Prenatal Companion |
| Organization | PrimeTek Africa - Codecamp Academy |
| Program | Advanced Full-Stack Software Development |
| Prepared By | Jonathan Shebirongo – Scrum Master and Sole Developer |
| Last Updated | 2026-11-27 |

**End of Document**

---

## Preparation Notes (not part of the formal minutes)

- The Sprint 02 backlog count is based on GitHub issues #12–#18: five closed and two open at sprint close.
- Story Point values were not available in the accessible issue information, so no Story Point totals or velocity have been invented.
- The repository tree contains the wireframe, activity, sequence, and component diagram files. The database and class diagram files were not present in the reviewed tree.
- The GitHub history shows the wireframe, activity, sequence, and component diagram commits on 2026-11-27.
- The report distinguishes GitHub issue closure from formal acceptance by the instructor.
- Sections 6, 9, and 10 from the supplied template have been intentionally omitted, as requested.
