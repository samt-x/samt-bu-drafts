---
# id: auto-generated – copied values are overwritten automatically on push
id: df6ebc64-e1d4-4fd7-a190-9f077eb085d2
title: "KF's analysis of use cases 1–19 in Digdir's Felles løft / SAMT-BU"
linkTitle: "Use case analysis"
weight: 10
lastmod: 2026-06-29T02:04:41+02:00
last_editor: Erik Hagen

---

> **Source:** Kommuneforlaget (KF), February 2026.
> [Open in Word Online](https://view.officeapps.live.com/op/view.aspx?src=https%3A%2F%2Fraw.githubusercontent.com%2FSAMT-BU%2Fsamt-bu-files%2Fmain%2Fcontributions%2F2026-02-24%20KFs%20analyse%20brukstilfeller%201%20til%2019%20i%20Digdirs%20Felles%20l%C3%B8ft%20-%20Sammenhengende%20tjenester%20for%20barn%20og%20unge%20eller%20SAMT-BU-prosjektet.docx&ui=en-US&rs=en-US) – [download Word file](https://github.com/SAMT-BU/samt-bu-files/raw/main/contributions/2026-02-24%20KFs%20analyse%20brukstilfeller%201%20til%2019%20i%20Digdirs%20Felles%20l%C3%B8ft%20-%20Sammenhengende%20tjenester%20for%20barn%20og%20unge%20eller%20SAMT-BU-prosjektet.docx)




Project «Felles løft: Coherent services for children and young people (the SAMT-BU project) with support from the co-financing scheme of the Norwegian Digitalisation Agency (Digdir).

Support: NOK 34 246 800.

The project is to establish a shared foundation for collaboration and knowledge about data-driven service development and seamless user journeys across levels of government and sectors, with piloting based on the area of children and young people – from kindergarten to higher education.

Below is the list of identified use cases in accordance with the template used in the work on the national architecture for children and young people and the standards of the Norwegian Directorate for Education and Training (Udir).

Source: Norwegian Digitalisation Agency (Digdir): Felles løft: Sammenhengende tjenester for barn og unge | Digdir

​

## SAMT-BU-001 – Making results from upper secondary education available


| **ID and title of ****use****-****case** | **SAMT-BU-001 – Making results from upper secondary education available** | Unique local identifier and title for the use case. The title should describe the goal as a short, active verb phrase. |
| --- | --- | --- |
| Brief description | The case addresses how results from upper secondary education can be made available in a better and more coherent way for actors who need the information in the further follow-up of young people. Results may, for example, be the status of completed education, completion, competence, assessments or documentation of the level achieved.The situation in focus is the transition from upper secondary education to the next phase of young people's life course, such as further education, work or follow-up services. In this phase it is crucial that relevant information is available at the right time, in the right form and for the right actor.Today it is often young people themselves who must help to communicate or document their own status. The case highlights how current practice and systems only to a limited extent support holistic availability and reuse of results information across services and levels of government. | Concise description of the use case, including context and scope. Describe what is included and what is outside (the black-box scope). |
| Primary actor | Young person completing upper secondary education (owner of their own results and needs for reuse/further follow-up) | The role that initiates the use case and holds the main goal. There shall be only one primary actor. |
| Secondary actors | Upper secondary school / county authority (produces and manages results information) School administration and competence systems (source system) Guidance and follow-up services (e.g. the follow-up service, NAV, higher education where relevant) Results service/portal (making available and access) | Other roles or systems that support or are affected by the use case. May be users or technical systems. |
| Stakeholders | Young people – easy access to their own status/competence and less documentation burden Counsellors/follow-up services – basis for decisions on the right measure at the right time School/county authority – correct, efficient and traceable management of results information Employers/educational institutions (where relevant) – verifiable documentation within purpose/legal basis Directorate/ministry – frameworks, quality, reporting and standardisation | Names of stakeholders and their primary interest in the goal the use case describes. There may be several stakeholders. |
| Specific considerations (overall) | Today, information about results from upper secondary education is often spread across several systems and available in different formats. It is not always clear who has access to which information, when the information is available, or how it can be used further.  This means that: information must be obtained manually or obtained again staff lack an overview in guidance and follow-up work young people themselves must explain or document their own status several times Breaks in information flow and responsibility arise in particular: when young people move on to work, higher education or follow-up serviceswhen different actors need the same information, but for different purposes when it is unclear who is responsible for making information availablewhen systems and work processes do not support reuse of existing data  For young people: Lack of overview of their own status and competence Need to document or explain their own situation several times Risk of delayed or inadequate guidance and follow-up  For staff in the services: Extra work related to manual collection and checking of information Uncertainty in the basis for decisions on guidance and follow-up Risk of errors or misunderstandings relating to results and competence  For the organisations: Inefficient use of time and resources Failure to make use of information that already exists Reduced quality and consistency in the data basis | Particular implications and considerations beyond general legal and architecture requirements, e.g. relating to AI, privacy, security and universal design. |
| Accessibility | Plain language and universal design in the presentation of results (comprehensibility for young people) Equal access across channels/devices and support for different languages/competence levels where relevant | Identified considerations relating to universal design and accessibility for different user groups. |
| Generative AI | Possible use: explaining results/competence in plain language, generating draft guidance, or identifying «next steps» as suggestions Requirements: human control, verifiability (what the advice is based on), and clear delimitation from automated decisions | Identified considerations relating to the use of generative AI, e.g. transparency, verifiability, bias and human control. |
| Diagram | USER FLOW  [Young person] -> [Upper secondary school] -> [Access to results] -> [Further education/work/OT]DATA FLOW  [School admin./competence system] -> (API) -> [Results service/portal]  [Results service] -> (role-/purpose-based access) -> [NAV/OT/higher education] | Visualisation showing the data flow between actors and system components that enable the use case. Use the recommended symbol set (cf. Appendix C2). |
| Implications for interoperability | Data flows that must be supported (min.): Access for young people to results/competence across services Role- and purpose-based sharing for follow-up/guidance (only the necessary amount of data) Events/status changes (e.g. completed/not completed, competence achieved) to authorised recipients Traceability: logging, versioning and source reference to the source system Interoperability needs (conceptual): Shared concepts and information model for «result», «competence», «completion» and «documentation» Standardised APIs and/or events, as well as a shared profile for identity/access (IAM) | Identification of which data flows must be supported, and which interoperability standards should be used where possible. |
| Notes | Source document (step 2): 01 Kunnskapsoversikt.docx | Supplementary notes and references used or mentioned elsewhere in the table. |


### Rationale (analysis) – SAMT-BU-001


*Making results from upper secondary education available*

#### UFO – ontological clarification


The use case establishes a clear distinction between information that belongs to the individual and information that is managed by the public sector. Results and competence are linked to the young person as an individual, but are produced and maintained within an institutional framework. This means that the challenge in the case is not about a lack of information, but about how managed information can be made available in a controlled way. Ontologically, this is therefore a service for making information available and reusing it, not a task that should rest with the individual young person.

#### Legal method


The main legal challenge in the case is not whether information can be shared, but how different purposes can be handled without undermining privacy and legal certainty. The use case points out that current practice in reality shifts the responsibility for clarifying purpose onto young people themselves. The analysis indicates that this should be replaced by clear authorisation mechanisms in which access is determined by role and purpose, not by manual documentation or consent in each individual situation. This strengthens both equal treatment and verifiability.

#### Toulmin – implicit argumentation


The underlying argument in the use case is that the quality of follow-up is weakened when authoritative information is not available where decisions are made. The grounds for this claim lie in repeated breaks in the information flow between school, guidance and follow-up. The qualifications in the argument are not about the wish for better availability, but about the risk of wrongful access and oversharing. The case thus implicitly argues for structured availability rather than informal exchange of information.

#### SWOT – strategic assessment


The analysis shows that the greatest weakness of the current situation is a lack of clarity in the responsibility for making information available. At the same time, the greatest strength lies in the fact that the benefit for both young people and the services is immediate and easy to understand. The opportunity in the case lies in the fact that the mechanisms for making information available can be reused in several transition situations, while the greatest threat is that the solution becomes fragmented if it is not anchored organisationally and financially.

#### iStar – goals and dependencies


The use case reveals an unfortunate dependency in which young people in practice act as information carriers between services. This dependency creates both a burden and a risk. The analysis points out that this role should be moved away from the individual and over to a shared service, so that the young person's role is limited to access to and use of their own data. At the same time, guidance and follow-up services become dependent on the information being available in the right form, which highlights the need for a shared solution.

#### TOGAF / ArchiMate – architecture implications


The architecture implication of the use case is that making results information available should be realised as a shared application service, not as point-to-point integrations between individual actors. Such an approach provides better conditions for access control, traceability and further development, and reduces the risk of young people becoming a manual link in the information flow.

#### KF extended NIF/EIF – interoperability


The case clearly shows that technical collaboration alone is not sufficient. Even with good interfaces, a lack of shared conceptual understanding and unclear responsibility will limit the effect. The analysis therefore points to the need for coordinated efforts on the competence and funding side as well, so that the solution can be managed and further developed as a lasting shared component.

#### Brief assessment


SAMT-BU-001 reveals a structural vacuum of responsibility in the transition from education to the rest of the life course. The case shows that coherent services do not primarily require new data, but clear responsibility for making existing, authoritative information available in a controlled and fair way.

## SAMT-BU-002 – Seamless transition from primary and lower secondary school to upper secondary education


| **ID and title of ****use****-****case** | **SAMT-BU-002 – Seamless transition from primary and lower secondary school to upper secondary education** | **Unique local identifier and title for the ****use case****. The title should describe the goal as a short, active verb phrase.** |
| --- | --- | --- |
| Brief description | The case addresses the transition from lower secondary school to upper secondary education – one of the most central transitions in the life course of children and young people. The transition involves both a change in everyday school life and a formal shift of responsibility from municipality to county authority, and affects many actors, services and systems.For young people, this is a phase marked by expectations, choices and increased responsibility for their own everyday life. For parents and guardians, it is about the reassurance that the child receives the right follow-up. For staff in school and the support services, it is about providing a good service, often under time pressure and with a limited overview.In this transition there is a need for relevant information to follow the pupil in a safe, precise and understandable way – without the pupil or parents and guardians themselves having to act as information carriers between actors. The case highlights how current practice and systems only to a limited extent support this need. | Concise description of the use case, including context and scope. Describe what is included and what is outside (the black-box scope). |
| Primary actor | • Pupil (or parent/guardian) | The role that initiates the use case and holds the main goal. There shall be only one primary actor. |
| Secondary actors | • Lower secondary school (municipality)• Upper secondary school (county)• PPT/OT• School administration systems | Other roles or systems that support or are affected by the use case. May be users or technical systems. |
| Stakeholders | • Pupil/parent or guardian – safe transition• Municipality/county – right follow-up• PPT/OT – access to relevant info• Authorities – compliance and quality | Names of stakeholders and their primary interest in the goal the use case describes. There may be several stakeholders. |
| Specific considerations (overall) | Today, many experience that the transition between lower secondary school and upper secondary school is not well enough supported by a coherent information flow. Important knowledge about the pupil's school career, need for adaptation, previous measures or follow-up often does not become available to the right actor at the right time.This means that information must be obtained again or reassessed, and that follow-up may be delayed or inadequate.Breaks arise in particular:when responsibility moves from the municipality to the county authoritywhen different services and levels of government have different understandings of concepts, roles and responsibilitieswhen specialist systems and work processes are not adapted to collaboration across boundarieswhen there is uncertainty about what information can, should and must be sharedFor end users (young people and parents and guardians):Insecurity in an already demanding transitionNeed to explain their situation and needs several timesRisk of delayed or inadequate follow-upFor staff in the services:Extra work related to manual coordinationLack of a complete overview and uncertainty in decisionsRisk that measures are not continued or come too lateFor the organisations:Inefficient use of time and resourcesIncreased risk of errors, delays and dropout | Particular implications and considerations beyond general legal and architecture requirements, e.g. relating to AI, privacy, security and universal design. |
| Accessibility | • Plain language and universal design• Support for different competence levels/languages where relevant | Identified considerations relating to universal design and accessibility for different user groups. |
| Generative AI | • Clarify area of use (drafting/classification/decision support)• Human control and verifiability | Identified considerations relating to the use of generative AI, e.g. transparency, verifiability, bias and human control. |
| Diagram | USER FLOW  [Pupil/parent or guardian] -> [Lower secondary school] -> [Transfer/access] -> [Upper secondary school] -> [Follow-up]DATA FLOW  [School admin. (municipality)] -> (standardised transfer) -> [School admin. (county)]  [PPT/OT] <-> (access-controlled sharing) <-> [School] : measures/adaptation (minimised) | Visualisation showing the data flow between actors and system components that enable the use case. Use the recommended symbol set (cf. Appendix C2). |
| Implications for interoperability | Breaks in information flow/responsibility (from source text):Breaks arise in particular:when responsibility moves from the municipality to the county authoritywhen different services and levels of government have different understandings of concepts, roles and responsibilitieswhen specialist systems and work processes are not adapted to collaboration across boundarieswhen there is uncertainty about what information can, should and must be sharedData flows that must be supported: identity/access, core information for the use case, status changes/events, and traceable logging. | Identification of which data flows must be supported, and which interoperability standards should be used where possible. |
| Notes | Elaboration/link: 02 Sømløs overgang grunnskole-videregående.docxSource document (step 2): 02 Sømløs overgang grunnskole-videregående.docx | Supplementary notes and references used or mentioned elsewhere in the table. |


### Rationale (analysis) – SAMT-BU-002


*Seamless transition between primary and lower secondary school and upper secondary education*

#### UFO – ontological clarification


This use case does not describe a single event, but a **transition situation** in which responsibility, information and expectations shift between organisational contexts. Ontologically, it is about continuity in service delivery to the same individual, despite several institutions being involved. The analysis shows that the challenge is not a lack of information about the pupil, but a lack of coherence in how this information is understood and used across school stages. The transition thus appears as a break in service rather than a pedagogical break.

#### Legal method


Legally, the use case highlights a tension between the need for early and relevant follow-up and the requirements of purpose limitation and data minimisation. Information that is legitimate in the context of primary and lower secondary school cannot automatically be carried over to upper secondary education without a clear clarification of purpose and responsibility. The analysis points out that current practice relies largely on manual assessments and local routines, which increases the risk of inconsistent practice and a lack of predictability for pupils.

#### Toulmin – implicit argumentation


The implicit claim in the use case is that the quality of the transition is weakened when the upper secondary school does not have sufficient understanding of the pupil's needs at the start. The grounds for this claim lie in the description of a lacking information flow and late identification of needs. The qualifications relate to the risk of transferring more information than necessary. The case therefore argues for better structure and timing in information sharing, not for more extensive sharing.

#### SWOT – strategic assessment


The strength of this use case lies in the clear potential for benefits: earlier and more targeted follow-up of pupils in a vulnerable transition. At the same time, a weakness is revealed in the form of fragmented responsibility between school owner, school management and support services. The opportunity lies in establishing a shared understanding and routines that can be used in all transitions, while the threat is that a lack of national or regional coordination leads to continued variation in practice.

#### iStar – goals and dependencies


The analysis reveals that the upper secondary school depends on relevant and understandable information in order to make adaptations early, while the pupil depends on these adaptations happening without having to explain their own situation again. This creates an asymmetric dependency in which the pupil's needs are not always picked up in time. The use case points towards this dependency being handled through better structures for information flow, so that the responsibility for coherence is not placed on the pupil.

#### TOGAF / ArchiMate – architecture implications


The architecture implication of the use case is that transition information must be handled as part of a holistic information architecture, not as local documents or informal dialogue. This points to a need for shared concepts, clear information objects and standardised mechanisms for transfer or making information available. Such an approach facilitates more predictable processes at the start of school and reduces the need for manual follow-up.

#### KF extended NIF/EIF – interoperability


The use case shows that a lack of collaboration in transitions is primarily an organisational and semantic problem, not a technical one. Without a shared understanding of what kind of information is relevant, and who is responsible for using it, technical solutions will have a limited effect. The analysis therefore points to the need for both competence development and clear funding of shared solutions that can support the transitions over time.

#### Brief assessment


SAMT-BU-002 makes clear that coherent services in the education pathway require transitions to be treated as service situations in their own right with clear frameworks. The use case shows that better coherence does not necessarily require more information, but better structure, timing and responsibility for the information that already exists.

.

## SAMT-BU-003 – ID management for refugees and use of Dnr (and transition to Fnr)


| **ID and title of ****use****-****case** | **SAMT-BU-003 – ID management for refugees and use of ****Dnr**** (and transition to ****Fnr****)** | **Unique local identifier and title for the ****use case****. The title should describe the goal as a short, active verb phrase.** |
| --- | --- | --- |
| Brief description | ID management for refugees and asylum seekersChange of IDSafeguarding the person's data and rights when changing ID number | Concise description of the use case, including context and scope. Describe what is included and what is outside (the black-box scope). |
| Primary actor | • Employee in a municipal service (caseworker/registrar) | The role that initiates the use case and holds the main goal. There shall be only one primary actor. |
| Secondary actors | • National Population Register/FIKS (identity service)• Municipal specialist systems• Integration platform | Other roles or systems that support or are affected by the use case. May be users or technical systems. |
| Stakeholders | • Children/young people/parents and guardians – access and rights• The municipality – correct case processing, data quality• System suppliers – support for ID change• Government actors – identity management | Names of stakeholders and their primary interest in the goal the use case describes. There may be several stakeholders. |
| Specific considerations (overall) | Within childhood and education there is no shared solution for assigning ID numbers to persons who have not yet received a D-number or F-number in the National Population Register. As a rule, parents receive a D-number in connection with having to pay tax, while it may take longer before children receive a D-number or national identity number. Pending this, the municipalities must register a number of fictitious national identity numbers according to their own regulations. The person objects thus potentially arise with a number of different identifiers around the public sector.The municipalities provide services to persons who are not registered in the National Population Register with a D-number or F-number. Municipalities are thus forced, each in their own sectors, to create one or many fictitious versions of these person objects pending these persons receiving an ID number in the National Population Register. There is no coordination of such fictitious numbers between sectors or between the various municipalities and county authorities.End users;children, young people, parents and guardians,Staff in the «services»Specialist system suppliersPremise setters: interest organisation, directorate, ministry and any othersHow are the actors affected by the current situation, and what are any consequencesBecause each individual municipality, or public body, has a duty and a self-interest in keeping track of person objects in the various IT systems, the administration spends a fair amount of time manually linking registered children to the new correct person objects after parents have typically received a D-number or F-number before their children. This is time-consuming and can cause uncertainty.The municipalities have a duty to provide persons with a number of services, such as kindergarten places and school places, even if they do not have an ID in the National Population Register.When persons eventually receive an ID number in the National Population Register, there is nothing automatic that lets the municipality say with certainty that new person objects imported from the National Population Register are, with 100% certainty, the same as those the municipality has registered in the various systems with a fictitious number. Only similarity in name and address can give some degree of indication of this. Errors can, in the worst case, occur. It is a little easier when the child eventually receives a D-number or national identity number, because then the parental relationships usually also follow in the data flow from the National Population Register. Unfortunately, this often happens long after the parents receive such a number in the National Population Register.Many systems support the transition from D-number to F-number in that the integration provides information about the change. This enables automation of the change, and thereby potentially ensures that data is not lost or made unavailable.The ID number is usually the primary key for person objects. So without automation or good control, duplicates of person objects will typically arise in several systems. This can mean that information is not found, such as decisions, or that parents or pupils lose data they have stored in various IT systems.Fictitious numbers also do not give access to log in to public IT systems with ID-porten.Health has come further with a shared solution here, as I understand it, and has something called Hjelpenummer. Read more about it here, as well as the challenges they describe, which can well be compared with other public sectors:https://www.nrk.no/norge/darlig-id-system-en-pasientfare-1.11425318 | Particular implications and considerations beyond general legal and architecture requirements, e.g. relating to AI, privacy, security and universal design. |
| Accessibility | • Plain language and universal design• Support for different competence levels/languages where relevant | Identified considerations relating to universal design and accessibility for different user groups. |
| Generative AI | • Clarify area of use (drafting/classification/decision support)• Human control and verifiability | Identified considerations relating to the use of generative AI, e.g. transparency, verifiability, bias and human control. |
| Diagram | USER FLOW  [Parent or guardian/child] -> [Municipal service] -> [Registration in specialist system] -> [Update on new ID]DATA FLOW  [Specialist systems in municipality] <-> [National Population Register/FIKS] : identities/status changes  [Specialist system] -> [Integration layer] -> [Other specialist systems] : ID change (D->F) + linking | Visualisation showing the data flow between actors and system components that enable the use case. Use the recommended symbol set (cf. Appendix C2). |
| Implications for interoperability | Breaks in information flow/responsibility (from source text):The municipalities provide services to persons who are not registered in the National Population Register with a D-number or F-number. Municipalities are thus forced, each in their own sectors, to create one or many fictitious versions of these person objects pending these persons receiving an ID number in the National Population Register. There is no coordination of such fictitious numbers between sectors or between the various municipalities and county authorities.Data flows that must be supported: identity/access, core information for the use case, status changes/events, and traceable logging. | Identification of which data flows must be supported, and which interoperability standards should be used where possible. |
| Notes | Elaboration/link: 03 Case-håndtering av Dnr-v0.9.docxSource document (step 2): 03 Case-håndtering av Dnr-v0.9.docx | Supplementary notes and references used or mentioned elsewhere in the table. |


### Rationale (analysis) – SAMT-BU-003


*Handling and reuse of documentation relating to **Dnr** (case number)*

#### UFO – ontological clarification


This use case reveals that case numbers and associated documentation act as carriers of institutional memory across time and organisational boundaries. Ontologically, the challenge is not linked to the documents themselves, but to the relationship between case, documentation and actors over time. When documentation is tied too closely to individual systems or individual processes, the coherence that the case number is meant to ensure is broken. The case is thus about preserving continuity and identity in the work of the public administration, not just about efficient case processing.

#### Legal method


Legally, the use case points to a tension between the duty to archive, documentation requirements and the need for efficient reuse of information. When the same documentation is requested several times in different processes, the risk of inconsistency, incorrect use and lack of verifiability increases. The analysis indicates that correct handling of Dnr is not just an archiving question, but a question of legal certainty: it must be possible to trace what has been done, on what basis, and with what documentation, also when the information is reused in new contexts.

#### Toulmin – implicit argumentation


The implicit claim in the use case is that the quality of case processing is weakened when documentation cannot be retrieved and reused in an unambiguous way. The grounds for this claim lie in the description of manual handling, copying and re-registration of documents. The qualifications are not about whether documentation should be reused, but about how this can happen without undermining archive structure and traceability. The case thus argues for better structure and links, not for less documentation.

#### SWOT – strategic assessment


The strength of this use case is that the benefit of better handling of Dnr is clear for both staff and the organisation: less duplicated work and a better overview. At the same time, a weakness is revealed in current practice, where documentation often becomes fragmented between systems and processes. The opportunity lies in establishing shared mechanisms for referencing and reusing documentation, while the threat is that a lack of shared practice leads to loss of coherence and weakened trust in the case basis.

#### iStar – goals and dependencies


The analysis reveals that caseworkers depend on documentation being correctly linked to the right case in order to carry out their work efficiently and correctly. At the same time, the organisation as a whole depends on these links being maintained over time, also when cases involve several units. The use case points to a hidden dependency: when the links fail, the individual caseworker has to compensate manually, which increases risk and burden.

#### TOGAF / ArchiMate – architecture implications


The architecture implication of the use case is that case numbers and documentation must be treated as shared information objects with clear relationships, not as local attributes in individual applications. This points to a need for a more coherent information architecture in which case and documentation can be referenced across systems without losing context or traceability. Such an approach reduces the need for copying and strengthens the quality of case processing.

#### KF extended NIF/EIF – interoperability


The use case shows that the challenges surrounding Dnr are primarily organisational and semantic. Without a shared understanding of what a case number represents, and how documentation is to be linked and reused, technical solutions alone will have a limited effect. The analysis therefore points to the need for both competence building and clear responsibility for managing the case structure, so that collaboration can take place in a predictable and verifiable way.

#### Brief assessment


SAMT-BU-003 makes clear that coherent services require continuity in documentation over time. The case shows that the case number is more than an administrative aid – it is a key to legal certainty, efficiency and trust in the public administration.

## SAMT-BU-004 – Relocation of pupils during the school year between municipalities/county authorities


| **ID and title of ****use****-****case** | **SAMT-BU-004 – Relocation of pupils during the school year between municipalities/county authorities** | **Unique local identifier and title for the ****use case****. The title should describe the goal as a short, active verb phrase.** |
| --- | --- | --- |
| Brief description | The use case concerns: Relocation of pupils during the school year between municipalities/county authorities. (Based on the case register.) | Concise description of the use case, including context and scope. Describe what is included and what is outside (the black-box scope). |
| Primary actor | (to be clarified) | The role that initiates the use case and holds the main goal. There shall be only one primary actor. |
| Secondary actors | • (to be clarified) | Other roles or systems that support or are affected by the use case. May be users or technical systems. |
| Stakeholders | • (to be clarified) | Names of stakeholders and their primary interest in the goal the use case describes. There may be several stakeholders. |
| Specific considerations (overall) | To be clarified. | Particular implications and considerations beyond general legal and architecture requirements, e.g. relating to AI, privacy, security and universal design. |
| Accessibility | • (to be clarified)• (to be clarified) | Identified considerations relating to universal design and accessibility for different user groups. |
| Generative AI | • (to be clarified)• (to be clarified) | Identified considerations relating to the use of generative AI, e.g. transparency, verifiability, bias and human control. |
| Diagram | USER FLOW (conceptual)  [End user] --> [Service/Front end] --> [Caseworker/Adviser] --> [Decision/Follow-up]DATA FLOW (conceptual)  [Client/portal] -> [Specialist system A] -> (API/Event) -> [Specialist system B] -> [Reporting/Log] | Visualisation showing the data flow between actors and system components that enable the use case. Use the recommended symbol set (cf. Appendix C2). |
| Implications for interoperability | To be clarified. | Identification of which data flows must be supported, and which interoperability standards should be used where possible. |
| Notes | (no notes in the case register) | Supplementary notes and references used or mentioned elsewhere in the table. |


### Rationale (analysis) – SAMT-BU-004


*Collaboration between services for children and young people with complex needs*

#### UFO – ontological clarification


This use case makes visible that the challenge does not lie in one single service, but in the interplay between several simultaneous services directed at the same child or young person. Ontologically, the case is about the coordination of roles, responsibilities and measures around one and the same person, where each actor sees only parts of the whole. The analysis shows that the absence of a shared understanding of the situation leads to parallel and partly conflicting measures, rather than a unified service delivery.

#### Legal method


Legally, the use case brings to the fore the interfaces between the duty of confidentiality, information sharing and the need for proper follow-up. When several services are involved at the same time, uncertainty easily arises about what can be shared, with whom and for what purpose. The analysis points out that this uncertainty often leads either to overly restrictive practice or to informal information exchange. Both weaken legal certainty and predictability for the child and the family.

#### Toulmin – implicit argumentation


The implicit claim in the use case is that lack of coordination between services reduces the effect of measures, even when each individual service does «the right thing» within its mandate. The grounds for this claim lie in the description of overlapping responsibilities and the lack of an overall picture. The qualifications relate to the risk of unwanted information sharing, which means that the case argues for better structures for collaboration, not for unlimited sharing.

#### SWOT – strategic assessment


The strength of this use case is that the need for better collaboration is clear and recognised by all the actors involved. At the same time, a weakness is revealed in the form of fragmented governance and a lack of shared arenas for coordination. The opportunity lies in establishing shared practice and support tools that can be used across services, while the threat is that unclear responsibilities and silo organisation persist if the measures are not anchored at management level.

#### iStar – goals and dependencies


The analysis makes visible mutual dependencies between services that today are often unspoken. Each actor depends on others following up their parts of the responsibility, while the child and the family depend on the services appearing coordinated. The use case points out that when these dependencies are not explicit, the coordination responsibility in practice falls on the family itself, which is both unreasonable and ineffective.

#### TOGAF / ArchiMate – architecture implications


The architecture implication of the use case is that collaboration cannot be based on ad hoc communication alone. There is a need for shared information structures and support for the coordination of measures, so that the actors can work from a shared situational picture. Such an architectural approach facilitates better coherence between business processes across services.

#### KF extended NIF/EIF – interoperability


The use case clearly shows that interoperability is first and foremost a question of organisation, competence and governance. Without a shared understanding of roles, responsibilities and goals, technical solutions alone will not have the desired effect. The analysis therefore points to the need for competence development and clear governance structures that support interdisciplinary cooperation over time.

#### Brief assessment


SAMT-BU-004 shows that coherent services for children and young people with complex needs require more than good stand-alone measures. The case underlines that holistic follow-up requires clear coordination, shared understanding and structures that support collaboration across organisational boundaries.

## SAMT-BU-005 – Consent portal (centralised overview of consents) (Further development of FIKS consent?)


| **ID and title of ****use****-****case** | **SAMT-BU-005 – Consent portal (centralised overview of consents) (Further development of FIKS consent?)** | **Unique local identifier and title for the ****use case****. The title should describe the goal as a short, active verb phrase.** |
| --- | --- | --- |
| Brief description | ID handling of refugees and asylum seekersChange of IDSafeguarding the person's data and rights when the ID number changes | Concise description of the use case, including context and scope. Describe what is included and what is outside (the black-box scope). |
| Primary actor | • Employee in a municipal service (caseworker/registrar) | The role that initiates the use case and holds the main goal. There shall be only one primary actor. |
| Secondary actors | • National Population Register/FIKS (identity service)• Municipal specialist systems• Integration platform | Other roles or systems that support or are affected by the use case. May be users or technical systems. |
| Stakeholders | • Children/young people/parents and guardians – access and rights• The municipality – correct case processing, data quality• System suppliers – support for ID change• Government actors – identity management | Names of stakeholders and their primary interest in the goal the use case describes. There may be several stakeholders. |
| Specific considerations (overall) | In childhood and education there is no common solution for assigning ID numbers to persons who have not yet received a D-number or F-number in the National Population Register. As a rule, parents receive a D-number in connection with having to pay tax, while it may take longer before children receive a D-number or national identity number. Pending this, the municipalities must register a number of fictitious national identity numbers according to their own regulations. Person objects thus potentially arise with a number of different identifiers across the public sector.The municipalities provide services to persons who are not registered in the National Population Register with a D-number or F-number. Municipalities are therefore forced, each in their own sectors, to create one or many fictitious versions of these person objects pending these persons receiving an ID number in the National Population Register. There is no coordination of such fictitious numbers between sectors or between the various municipalities and county authorities.End users;children, young people, parents and guardians,Employees in the «services»Specialist system suppliersPremise setters: interest organisation, directorate, ministry and any othersHow are the actors affected by the current situation, and what are any consequencesSince each individual municipality, or public administration body, has a duty and a self-interest in keeping track of person objects in the various IT systems, this leads to the administration spending a fair amount of time manually linking registered children to the new correct person objects after parents have typically received a D-number or F-number before their children. This is time-consuming and may cause uncertainty.The municipalities have a duty to provide persons with a number of services, such as kindergarten places and school places, even if they have no ID in the National Population Register.When persons eventually receive an ID number in the National Population Register, there is nothing automatic that allows the municipality to say with certainty that new person objects imported from the National Population Register are with 100% certainty the same as those the municipality has registered in the various systems with a fictitious number. Only similarity in name and address can give a degree of indication of this. In the worst case, errors may occur. It is somewhat easier when the child eventually receives a D-number or national identity number, because then the parent relationships usually also follow in the data flow from the National Population Register. Unfortunately, this often happens long after the parents receive such a number in the National Population Register.Many systems support the transition from D-number to F-number in that the integration provides information about the change. This enables the change to be automated, and one then potentially ensures that data is not lost or made inaccessible.The ID number is usually the primary key for person objects. So without automation or good control, duplicates of person objects will typically arise in several systems. This may mean that information is not found, such as decisions, or that parents or pupils lose data they have stored in various IT systems.Fictitious numbers also do not give access to log in to public IT systems with ID-porten.Health has come further with a common solution here, as I understand it, and has something called Hjelpenummer. Read more about it here, as well as the challenges they describe, which can well be compared with other public sectors:https://www.nrk.no/norge/darlig-id-system-en-pasientfare-1.11425318 | Particular implications and considerations beyond general legal and architecture requirements, e.g. relating to AI, privacy, security and universal design. |
| Accessibility | • Plain language and universal design• Support for different competence levels/languages where relevant | Identified considerations relating to universal design and accessibility for different user groups. |
| Generative AI | • Clarify area of use (draft/classification/decision support)• Human control and verifiability | Identified considerations relating to the use of generative AI, e.g. transparency, verifiability, bias and human control. |
| Diagram | USER FLOW  [Parent or guardian/child] -> [Municipal service] -> [Registration in specialist system] -> [Update on new ID]DATA FLOW  [Specialist systems in municipality] <-> [National Population Register/FIKS] : identities/status changes  [Specialist system] -> [Integration layer] -> [Other specialist system] : ID change (D->F) + linking | Visualisation showing the data flow between actors and system components that enable the use case. Use the recommended symbol set (cf. Appendix C2). |
| Implications for interoperability | Breaks in information flow/responsibility (from source text):The municipalities provide services to persons who are not registered in the National Population Register with a D-number or F-number. Municipalities are therefore forced, each in their own sectors, to create one or many fictitious versions of these person objects pending these persons receiving an ID number in the National Population Register. There is no coordination of such fictitious numbers between sectors or between the various municipalities and county authorities.Data flows that must be supported: identity/access, core information for the use case, status changes/events, and traceable logging. | Identification of which data flows must be supported, and which interoperability standards should be used where possible. |
| Notes | Source document (step 2): 03 Case-håndtering av Dnr-v0.9.docx | Supplementary notes and references used or mentioned elsewhere in the table. |


### Rationale (analysis) – SAMT-BU-005


*Consent portal (centralised overview of consents)*

#### UFO – ontological clarification


This use case reveals a classic ontological distinction between **the person** and **the identifiers** used to represent the person in different systems. The practical challenge is not a «lack of ID», but that several systems treat the ID as if it *is* the person. When the identifier changes (from local/temporary to D-/F-number), the relationships between person and data become fragile. The analysis therefore points out that the core is **identity continuity over time**: the same individual must be traceable as the same “bearer” of rights, obligations and history, even if the identifier changes.

**Important quality point:** The title and content point in slightly different directions (the title refers to a consent portal, while the content is about ID/identity change). The UFO analysis suggests that you should clarify which phenomenon the case actually describes, so that the table's “goal” (title) and “scope” (description/considerations) are tightly aligned.

#### Legal method


The legal risk lies in what happens when a change of identifier leads to **breaks in the management of rights**: access, right of access, record/archive trails and service provision can go wrong if data is either not linked or linked incorrectly. This becomes particularly demanding when it concerns children/parents and guardians, because responsibility, representation and access are often conditional and time-limited. Legally, the case points to a need for **verifiable identity management**: one must be able to document which identity applied when, and on what basis links were made. This reduces the risk of incorrect service provision and weak legal certainty.

#### Toulmin – implicit argumentation


In practice, the case argues that the quality of municipal service provision is weakened when identity cannot be handled as a stable “bearer” of data over time. The implicit reasoning is that a controlled mechanism for identity change and linking results in fewer errors and less manual work. The qualifications lie in the fact that any link must be correct, and that an incorrect link can be worse than a missing link. The argumentation therefore points towards a governed process and traceability, not “automation without control”.

#### SWOT – strategic assessment


The strategic weakness the case points to is that the municipalities are in practice forced into local variants of identity management, which results in fragmentation and varies from system to system. The strength is that the benefit of shared practice is clear and direct: less manual follow-up, fewer errors, more robust data. The opportunity lies in establishing a shared identity and change mechanism that can be reused across services. The threat is that differing implementation among vendors and lack of governance create lasting “scars” in the data foundation.

#### iStar – goals and dependencies


The use case makes visible a critical dependency: the municipal caseworker's ability to provide a correct service depends on the identity change being handled consistently in all affected systems. When this dependency is not resolved by shared mechanisms, the burden is shifted to the individual employee (manual updates, double registration, checks). At the same time, the citizen (children/parents and guardians) becomes indirectly dependent on the municipality managing to “carry” the history forward. The analysis therefore points out that the goal of correct service production and the goal of reduced burden must be achieved by moving the dependency from individuals to managed components.

#### TOGAF / ArchiMate – architecture implications


The architecture implication is that identity must be handled as a **cross-cutting capability** (master data/identity resolution), not as a function in each specialist system. The case points to a need for a mechanism that handles identity change as a controlled event, with consistent updating and traceability across integrations. This suggests an architecture pattern in which specialist systems do not “own” identity alone, but relate to a shared identity reference and change logic.

#### KF extended NIF/EIF – interoperability


The case clearly illustrates that this is an interoperability challenge along several axes at the same time: semantic (what identity/ID means in practice), organisational (who is responsible in the event of a change), technical (how to propagate changes), and legal (what requirements apply to documentation and control). KF's extensions become particularly relevant here: competence, because employees and vendors must understand the implications of identity change, and economy, because this is rarely solved sustainably without shared funding and management (otherwise it becomes “local patches” in each system).

#### Brief assessment


SAMT-BU-005 points to a fundamental prerequisite for coherent services: identity must withstand change without data and rights “cracking”. The case also has a clear point for improvement in the documentation: make the title/goal and description/scope consistent, so that the analysis and later measures target the same phenomenon.

## SAMT-BU-006 – Centralised access to data parents need (NP, mapping assessments, final assessment etc.)


| **ID and title of ****use****-****case** | **SAMT-BU-006 – Centralised access to data parents need (NP, mapping assessments, final assessment ****etc.****)** | **Unique local identifier and title for the ****use case****. The title should describe the goal as a short, active verb phrase.** |
| --- | --- | --- |
| Brief description | The use case concerns: Centralised access to data parents need (NP, mapping assessments, final assessment etc.). (Based on the case register.) | Concise description of the use case, including context and scope. Describe what is included and what is outside (the black-box scope). |
| Primary actor | • School leader/head teacher (coordinates measures and follow-up) | The role that initiates the use case and holds the main goal. There shall be only one primary actor. |
| Secondary actors | • Teachers• PPT• Parents and guardians• Collaboration tool (BTI/stafettlogg-like)• IAM/access management | Other roles or systems that support or are affected by the use case. May be users or technical systems. |
| Stakeholders | • Pupil/parent or guardian – rights and understandable collaboration• School/PPT – effective and safe follow-up• Management – overview, allocation, approval• Supervisory authority – compliance (duty of confidentiality/consent) | Names of stakeholders and their primary interest in the goal the use case describes. There may be several stakeholders. |
| Specific considerations (overall) | To be clarified. | Particular implications and considerations beyond general legal and architecture requirements, e.g. relating to AI, privacy, security and universal design. |
| Accessibility | • Plain language• Multiple languages/channels (text/audio/image) where relevant | Identified considerations relating to universal design and accessibility for different user groups. |
| Generative AI | • Decision support/drafts only, with human control• Requirements for transparency/source basis for suggestions | Identified considerations relating to the use of generative AI, e.g. transparency, verifiability, bias and human control. |
| Diagram | USER FLOW  [Parent or guardian] <-> [School] <-> [PPT] : holistic pupil follow-up (coordinated)DATA FLOW  [Collaboration tool] -> [Role-based access] -> [Measures/tasks]  [School/PPT system] <-> (standardised data) <-> [Management data/insight] | Visualisation showing the data flow between actors and system components that enable the use case. Use the recommended symbol set (cf. Appendix C2). |
| Implications for interoperability | Data flows that must be supported: identity/access, core information for the use case, status changes/events, and traceable logging. | Identification of which data flows must be supported, and which interoperability standards should be used where possible. |
| Notes | Source document (step 2): 18 Case fra UDE i Oslo kommune.docx | Supplementary notes and references used or mentioned elsewhere in the table. |


### Rationale (analysis) – SAMT-BU-006


*Holistic overview of measures and follow-up for children and young people*

#### UFO – ontological clarification


This use case makes visible an ontological distinction between **measures as events** and **follow-up as an ongoing state**. In current practice, measures are often registered as stand-alone activities in different systems, while the whole of the follow-up remains implicit and fragmented. Ontologically, this means that the information lacks a unifying perspective that links the measures together around the child or young person over time. The case is therefore not primarily about establishing new measures, but about making existing measures understandable as parts of a coherent follow-up.

#### Legal method


Legally, the use case raises questions of adequacy and documentation. When measures are implemented by different services without a shared overview, it becomes difficult to assess whether the follow-up as a whole is sufficient and coordinated. The analysis points out that a lack of overview does not necessarily entail a breach of the law in the individual service, but may lead to failure in the whole. This challenges both the legal certainty of the child and the municipality's ability to document that it has acted responsibly over time.

#### Toulmin – implicit argumentation


The implicit claim in the use case is that the quality of follow-up is weakened when measures are assessed in isolation, without insight into what other services are doing. The grounds for the claim lie in the description of parallel tracks and lack of coordination. The qualifications concern the fact that increased overview must not lead to unlawful access or information sharing. The case therefore argues for overview as decision support, not as general access to details.

#### SWOT – strategic assessment


The strength of this use case is that it addresses a concrete and recognisable problem for both employees and management: lack of overview creates a risk of both too many and too few measures. The weakness lies in the fact that the measures are often owned by different professional communities with their own systems and concepts. The opportunity lies in establishing a shared situational picture that can support interdisciplinary cooperation, while the threat is that lack of governance causes the overview to become incomplete or outdated.

#### iStar – goals and dependencies


The analysis makes visible that each individual service depends on other services following up their measures in a predictable way. At the same time, the child and the family depend on the services having an overview of each other, so that the follow-up is experienced as holistic. When this dependency is not supported by shared structures, the coordination responsibility is in practice shifted onto the family. The use case thus points to the need to move this dependency from people to systematically supported processes.

#### TOGAF / ArchiMate – architecture implications


The architecture implication of the use case is that an overview of measures must be realised as a layer above existing specialist systems, rather than as a new monolithic system. Such a solution presupposes clear information objects and update mechanisms that can retrieve status without copying details. This enables a shared situational picture while each specialist system retains its responsibility and its autonomy.

#### KF extended NIF/EIF – interoperability


The use case shows that interoperability here depends to a large extent on organisational and semantic maturity. Without a shared understanding of what is meant by “measure”, “follow-up” and “status”, technical solutions will quickly lose value. The analysis therefore points to the need for competence development and clear anchoring of responsibility for the overall overview, as well as financial frameworks that make it possible to manage such a solution over time.

#### Brief assessment


SAMT-BU-006 makes clear that holistic follow-up cannot be achieved through isolated measures alone. The case shows that coherent services require structures that make it possible to see measures in context, over time and across services, without this being at the expense of privacy or professional autonomy.

## SAMT-BU-007 – Early identification of pupils at risk and continuation of measures/data throughout the course of education


| **ID and title of ****use****-****case** | **SAMT-BU-007 – Early identification of pupils at risk and continuation of measures/data throughout the course of education** | **Unique local identifier and title for the ****use case****. The title should describe the goal as a short, active verb phrase.** |
| --- | --- | --- |
| Brief description | ID handling of refugees and asylum seekersChange of IDSafeguarding the person's data and rights when changing ID number | Concise description of the use case, including context and scope. Describe what is included and what is outside (the black-box scope). |
| Primary actor | • Employee in a municipal service (caseworker/registrar) | The role that initiates the use case and holds the main goal. There shall be only one primary actor. |
| Secondary actors | • National Population Register/FIKS (identity service)• Municipal specialist systems• Integration platform | Other roles or systems that support or are affected by the use case. May be users or technical systems. |
| Stakeholders | • Children/young people/parents and guardians – access and rights• The municipality – correct case handling, data quality• System suppliers – support for ID change• Central government actors – identity management | Names of stakeholders and their primary interest in the goal the use case describes. There may be several stakeholders. |
| Specific considerations (overall) | Within childhood and education there is no common solution for assigning ID numbers to persons who have not yet been given a D-number or F-number in the National Population Register. As a rule, parents receive a D-number in connection with having to pay tax, whereas it may take longer before children receive a D-number or national identity number. Pending this, the municipalities must register a number of fictitious national identity numbers according to their own arrangements. Person objects thus potentially arise with a number of different identifiers across the public sector.The municipalities provide services to persons who are not registered in the National Population Register with a D-number or F-number. Municipalities are thereby forced, each within its own sectors, to create one or many fictitious versions of these person objects pending these persons receiving an ID number in the National Population Register. There is no coordination of such fictitious numbers between sectors or between the various municipalities and county authorities.End users;children, young people, parents and guardians,Employees in the «services»Specialist system suppliersPremise setters: interest organisations, directorates, ministries and any othersHow are the actors affected by the current situation, and what are the possible consequencesBecause each individual municipality, or public body, has a duty and a self-interest in keeping track of person objects in the various IT systems, the administration spends a fair amount of time manually linking registered children to the new correct person objects after the parents have typically received a D-number or F-number before their children. This is time-consuming and may cause uncertainty.The municipalities have a duty to provide persons with a number of services, such as a kindergarten place and a school place, even if they have no ID in the National Population Register.When persons eventually receive an ID number in the National Population Register, there is nothing automatic that allows the municipality to say with certainty that new person objects imported from the National Population Register are with 100% certainty the same as those the municipality has registered in the various systems with a fictitious number. Only similarity in name and address can give some degree of indication of this. In the worst case, errors may occur. It is somewhat easier when the child eventually receives a D-number or national identity number, because then the parental relationships usually also follow in the data flow from the National Population Register. Unfortunately, this often happens long after the parents receive such a number in the National Population Register.Many systems support the transition from D-number to F-number in that the integration provides information about the change. This enables the change to be automated, and one then potentially ensures that data is not lost or made inaccessible.The ID number is usually the primary key for person objects. So without automation or good control, duplicates of person objects will typically arise in several systems. This may mean that information is not found, such as decisions, or that parents or pupils lose data they have stored in various IT systems.Fictitious numbers also do not give access to log in to public IT systems with ID-porten.Health has come further with a common solution here, as I understand it, and has something called Hjelpenummer. Read more about it here, as well as the challenges they describe, which can well be compared with other public sectors:https://www.nrk.no/norge/darlig-id-system-en-pasientfare-1.11425318 | Particular implications and considerations beyond general legal and architecture requirements, e.g. relating to AI, privacy, security and universal design. |
| Accessibility | • Plain language and universal design• Support for different levels of competence/languages where relevant | Identified considerations relating to universal design and accessibility for different user groups. |
| Generative AI | • Clarify area of use (drafting/classification/decision support)• Human control and verifiability | Identified considerations relating to the use of generative AI, e.g. transparency, verifiability, bias and human control. |
| Diagram | USER FLOW  [Parent or guardian/child] -> [Municipal service] -> [Registration in specialist system] -> [Update on new ID]DATA FLOW  [Specialist systems in municipality] <-> [National Population Register/FIKS] : identities/status changes  [Specialist system] -> [Integration layer] -> [Other specialist system] : ID change (D->F) + linking | Visualisation showing the data flow between actors and system components that enable the use case. Use the recommended symbol set (cf. Appendix C2). |
| Implications for interoperability | Breaks in information flow/responsibility (from source text):The municipalities provide services to persons who are not registered in the National Population Register with a D-number or F-number. Municipalities are thereby forced, each within its own sectors, to create one or many fictitious versions of these person objects pending these persons receiving an ID number in the National Population Register. There is no coordination of such fictitious numbers between sectors or between the various municipalities and county authorities.Data flows that must be supported: identity/access, core information for the use case, status changes/events, and traceable logging. | Identification of which data flows must be supported, and which interoperability standards should be used where possible. |
| Notes | Source document (step 2): 03 Case-håndtering av Dnr-v0.9.docx | Supplementary notes and references used or mentioned elsewhere in the table. |


### Rationale (analysis) – SAMT-BU-007


*Coordinated information flow between school, health and child welfare services*

#### UFO – ontological clarification


This use case makes clear that information flow between school, health and child welfare services cannot be understood as simple sharing of documents, but as coordination between **different normative practices** around the same child. Ontologically, each service represents its own sphere of action with its own purposes, assessment criteria and decision logic. The case shows that the challenge arises when these spheres of action touch the same child without the relationships between them being explicitly understood or managed.

#### Legal method


From a legal perspective, this is one of the most complex use cases, because it touches core areas such as the duty of confidentiality, the duty to provide information and consent. The analysis shows that uncertainty about the legal basis often leads either to overly restrictive information sharing or to informal practice. Both weaken legal certainty. The case points to the need for clearer structures that support correct assessment of when information sharing is necessary, lawful and proportionate.

#### Toulmin – implicit argumentation


The implicit claim in the use case is that the quality of follow-up is weakened when relevant services lack insight into each other's assessments and measures. The grounds for this claim lie in the description of lacking coordination and parallel assessment processes. The qualifications relate to the risk of unnecessary sharing of sensitive information. The case thus argues for precise and needs-driven information flow, not for general openness between services.

#### SWOT – strategic assessment


The strength of this use case is that it addresses an area where better collaboration can have great significance for the child's situation. At the same time, a considerable weakness is revealed in the form of differing practice and interpretation of regulations between services. The opportunity lies in establishing a shared understanding and support for legally correct assessments, while the threat is that lack of trust and fear of breaching rules lead to continued fragmentation.

#### iStar – goals and dependencies


The analysis reveals mutual dependencies between school, health and child welfare services that today are often informal and dependent on individuals. Each service depends on the others sharing relevant information when necessary, while the child depends on this collaboration taking place in a way that safeguards both needs and rights. The case points out that without support for handling these dependencies explicitly, collaboration will remain vulnerable.

#### TOGAF / ArchiMate – architecture implications


The architecture implication of the use case is that information flow between services must be supported by structures that safeguard both selective sharing and traceability. This points to the need for mechanisms that enable contextual access to information, rather than shared databases. Such an architecture can reduce risk and at the same time support better coordination in complex cases.

#### KF extended NIF/EIF – interoperability


The use case illustrates that interoperability here presupposes high legal and organisational maturity. Technology can support, but not replace, the need for competence in understanding regulations and shared practice. The analysis therefore points out that investments in collaboration must include both competence development and clear governance mechanisms, in addition to technical solutions.

#### Brief assessment


SAMT-BU-007 shows that coordinated efforts for children in vulnerable situations require more than goodwill between services. The case makes clear the need for structures that make it possible to collaborate correctly, precisely and verifiably, without setting aside considerations of privacy and legal certainty.

## SAMT-BU-008 – Transitions between levels of education (from kindergarten to primary and lower secondary school, on to upper secondary and higher education) – e.g. exchange


| **ID and title of ****use****-****case** | **SAMT-BU-008 – Transitions between levels of education (from kindergarten to primary and lower secondary school, on to upper secondary and higher education) – e.g. exchange** | **Unique local identifier and title for the ****use case****. The title should describe the goal as a short, active verb phrase.** |
| --- | --- | --- |
| Brief description | The case addresses the transition from lower secondary school to upper secondary education – one of the most central transitions in the life course of children and young people. The transition involves both a change in everyday school life and a formal transfer of responsibility from municipality to county authority, and affects many actors, services and systems.For young people, this is a phase marked by expectations, choices and increased responsibility for their own everyday lives. For parents and guardians, it is about the reassurance that the child receives the right follow-up. For employees in schools and support services, it is about providing a good offer, often under time pressure and with limited overview.In this transition there is a need for relevant information to follow the pupil in a safe, precise and understandable way – without the pupil or parents and guardians themselves having to act as information carriers between actors. The case sheds light on how current practice and systems only to a limited extent support this need. | Concise description of the use case, including context and scope. Describe what is included and what is outside (the black-box scope). |
| Primary actor | • Pupil (possibly parent or guardian) | The role that initiates the use case and holds the main goal. There shall be only one primary actor. |
| Secondary actors | • Lower secondary school (municipality)• Upper secondary school (county)• PPT/OT• School administration systems | Other roles or systems that support or are affected by the use case. May be users or technical systems. |
| Stakeholders | • Pupil/parent or guardian – safe transition• Municipality/county – correct follow-up• PPT/OT – access to relevant info• Authorities – compliance and quality | Names of stakeholders and their primary interest in the goal the use case describes. There may be several stakeholders. |
| Specific considerations (overall) | Today many people experience that the transition between lower secondary school and upper secondary school is not sufficiently supported by coherent information flow. Important knowledge about the pupil's school career, need for adaptations, previous measures or follow-up is often not available to the right actor at the right time.This means that information must be gathered again or reassessed, and that follow-up may be delayed or inadequate.Breaks occur in particular:when responsibility is transferred from municipality to county authoritywhen different services and levels of government have different understandings of concepts, roles and responsibilitieswhen specialist systems and work processes are not adapted to collaboration across boundarieswhen there is uncertainty about what information can, should and must be sharedFor end users (young people and parents and guardians):Insecurity in an already demanding transitionNeed to explain situation and needs several timesRisk of delayed or inadequate follow-upFor employees in the services:Extra work related to manual coordinationLack of overall overview and uncertainty in decisionsRisk that measures are not continued or come too lateFor the organisations:Inefficient use of time and resourcesIncreased risk of errors, delays and dropout | Particular implications and considerations beyond general legal and architecture requirements, e.g. relating to AI, privacy, security and universal design. |
| Accessibility | • Plain language and universal design• Support for different levels of competence/languages where relevant | Identified considerations relating to universal design and accessibility for different user groups. |
| Generative AI | • Clarify area of use (drafting/classification/decision support)• Human control and verifiability | Identified considerations relating to the use of generative AI, e.g. transparency, verifiability, bias and human control. |
| Diagram | USER FLOW  [Pupil/parent or guardian] -> [Lower secondary school] -> [Transfer/access] -> [Upper secondary school] -> [Follow-up]DATA FLOW  [School admin. (municipality)] -> (standardised transfer) -> [School admin. (county)]  [PPT/OT] <-> (access-controlled sharing) <-> [School] : measures/adaptations (minimised) | Visualisation showing the data flow between actors and system components that enable the use case. Use the recommended symbol set (cf. Appendix C2). |
| Implications for interoperability | Breaks in information flow/responsibility (from source text):Breaks occur in particular:when responsibility is transferred from municipality to county authoritywhen different services and levels of government have different understandings of concepts, roles and responsibilitieswhen specialist systems and work processes are not adapted to collaboration across boundarieswhen there is uncertainty about what information can, should and must be sharedData flows that must be supported: identity/access, core information for the use case, status changes/events, and traceable logging. | Identification of which data flows must be supported, and which interoperability standards should be used where possible. |
| Notes | Source document (step 2): 02 Sømløs overgang grunnskole-videregående.docx | Supplementary notes and references used or mentioned elsewhere in the table. |


### Rationale (analysis) – SAMT-BU-008


*Alerting and early identification of children and young people at risk*

**UFO – ontological clarification**

Ontologically, this use case concerns the transition from **observation** to **concern**, and on to **action**. Alerting is not in itself a measure, but a mechanism that makes it possible to establish a shared understanding of risk at an early stage. The case shows that risk is not an object that exists in isolation, but arises through the interpretation of signals in different services. The challenge therefore lies not in a lack of observations, but in a lack of structure for compiling and assessing them across services.

#### Legal method


From a legal perspective, alerting is a sensitive area, because it touches both the duty of confidentiality and the duty to provide information. The use case points out that uncertainty about the regulations often leads either to passivity or to informal practice. The analysis indicates that this can have serious consequences: intervention that comes too late or unfounded escalation. The case therefore points to the need for clear frameworks that support correct assessment of when a concern should be shared, and in what way, without undermining the legal certainty of the child and the family.

#### Toulmin – implicit argumentation


The implicit claim in the use case is that early identification of risk gives better opportunity for preventive measures. The grounds for this claim lie in the description of missed opportunities when signals are not picked up or not linked together. The qualifications relate to the danger of misjudgements and stigmatisation. The case thus argues for structured alerting as decision support, not as an automatic trigger of measures.

#### SWOT – strategic assessment


The strength of this use case is that the potential for prevention is considerable, both for the child and for society. At the same time, a weakness is revealed in the form of varying thresholds for concern and differing practice between services. The opportunity lies in establishing a shared understanding and support for the assessment of risk, while the threat is that lack of trust and unclear frameworks lead to either over- or under-reporting.

#### iStar – goals and dependencies


The analysis reveals that employees in different services depend on being able to express concern in a way that is understood and handled correctly by others. At the same time, the child depends on concerns leading to appropriate follow-up, not merely registration. The use case points out that when this dependency is not supported by shared structures, alerting becomes dependent on individuals and unpredictable.

#### TOGAF / ArchiMate – architecture implications


The architecture implication of the use case is that alerting must be supported by mechanisms that distinguish between registration, assessment and any follow-up. This points to the need for clear process steps and information objects, so that alerts can be handled systematically without creating unnecessary dissemination of sensitive information. Such an architecture supports both precision and traceability.

#### KF extended NIF/EIF – interoperability


The use case shows that interoperability in alerting situations depends to a large extent on shared competence and trust between services. Technology can contribute structure, but without a shared understanding of roles, responsibilities and thresholds the effect will be limited. The analysis therefore points to the need for coordinated training and clear anchoring of practice, in addition to technical solutions.

#### Brief assessment


SAMT-BU-008 makes clear that early intervention presupposes more than good intentions. The case shows that structured alerting and a shared understanding of risk are crucial to being able to intervene at the right time, in a way that safeguards both the child and legal certainty.

## SAMT-BU-009 – Changing school or place of study.


| **ID and title of ****use****-****case** | **SAMT-BU-009 – Changing school or place of study.** | **Unique local identifier and title for the ****use case****. The title should describe the goal as a short, active verb phrase.** |
| --- | --- | --- |
| Brief description | The use case concerns: Changing school or place of study.. (Based on the case register.) | Concise description of the use case, including context and scope. Describe what is included and what is outside (the black-box scope). |
| Primary actor | (to be clarified) | The role that initiates the use case and holds the main goal. There shall be only one primary actor. |
| Secondary actors | • (to be clarified) | Other roles or systems that support or are affected by the use case. May be users or technical systems. |
| Stakeholders | • (to be clarified) | Names of stakeholders and their primary interest in the goal the use case describes. There may be several stakeholders. |
| Specific considerations (overall) | To be clarified. | Particular implications and considerations beyond general legal and architecture requirements, e.g. relating to AI, privacy, security and universal design. |
| Accessibility | • (to be clarified)• (to be clarified) | Identified considerations relating to universal design and accessibility for different user groups. |
| Generative AI | • (to be clarified)• (to be clarified) | Identified considerations relating to the use of generative AI, e.g. transparency, verifiability, bias and human control. |
| Diagram | USER FLOW (conceptual)  [End user] --> [Service/Front end] --> [Caseworker/Adviser] --> [Decision/Follow-up]DATA FLOW (conceptual)  [Client/portal] -> [Specialist system A] -> (API/Event) -> [Specialist system B] -> [Reporting/Log] | Visualisation showing the data flow between actors and system components that enable the use case. Use the recommended symbol set (cf. Appendix C2). |
| Implications for interoperability | To be clarified. | Identification of which data flows must be supported, and which interoperability standards should be used where possible. |
| Notes | (no notes in the case register) | Supplementary notes and references used or mentioned elsewhere in the table. |


### Rationale (analysis) – SAMT-BU-009


*Coordinated transition from child welfare measures to ordinary municipal services*

#### UFO – ontological clarification


This use case concerns a transition where **measures cease**, but **the need for follow-up does not necessarily do so**. Ontologically, it is about a shift in service context for the same individual, where the role of «recipient of child welfare measures» ends, while the role of citizen in need of support continues. The case shows that a lack of coherence in this shift often leads to breaks in follow-up, not because information is missing, but because responsibility changes without sufficient coordination.

#### Legal method


From a legal perspective, the use case raises questions about the proper termination of measures and further follow-up. When the responsibility of the child welfare services formally ceases, a borderline area arises where the risk of «responsibility falling through the cracks» is high. The analysis points out that the lack of a structured transition may mean that relevant assessments and experience are not passed on in a lawful and necessary manner. This challenges both continuity in service provision and the legal certainty of the young person.

#### Toulmin – implicit argumentation


The implicit claim in the use case is that ending child welfare measures without a coordinated transition increases the risk that needs are not picked up in time. The grounds for this claim lie in the description of breaks between services and lacking transfer of insight. The qualifications concern the fact that information from child welfare services must be handled with care and shared only when necessary and relevant. The case thus argues for a structured transition, not for continuing the role of the child welfare services.

#### SWOT – strategic assessment


The strength of this use case is that it clearly addresses a known risk point in the service pathway. The weakness lies in transitions often being handled individually and without shared frameworks. The opportunity lies in establishing clear transition processes that can be used across cases, while the threat is that a lack of ownership of the transition phase leads to loss of important insight and reduced quality of follow-up.

#### iStar – goals and dependencies


The analysis reveals that both the child welfare service and other municipal services are mutually dependent on the transition being handled in a predictable way. The young person, at the same time, depends on responsibility actually being taken over, not merely formally ended. The use case points out that when this dependency is not supported by clear structures, the transition becomes dependent on individuals and vulnerable.

#### TOGAF / ArchiMate – architecture implications


The architecture implication of the use case is that the transition from child welfare measures should be supported by clear process and information mechanisms that mark termination and handover. This points to the need for shared process steps and information objects that can support the transition without disclosing more information than necessary. Such an architecture provides better control and traceability in the transition phase.

#### KF extended NIF/EIF – interoperability


The use case shows that interoperability in the transition from child welfare services depends strongly on organisational maturity and a clear understanding of roles. Technology can support handover, but without shared practice and competence, transitions will remain vulnerable. The analysis therefore points to the need for clear governance and competence building around transition processes, in addition to technical solutions.

#### Brief assessment


SAMT-BU-009 makes clear that ending child welfare measures is not an end point, but a critical moment of transition. The case shows that coherent services presuppose that responsibility and insight are passed on in a controlled and proper manner, so that the young person does not fall between services.

## SAMT-BU-010 – Transition to other municipal services such as child welfare services or PPT.


| **ID and title of ****use****-****case** | **SAMT-BU-010 – Transition to other municipal services such as child welfare services or PPT.** | **Unique local identifier and title for the ****use case****. The title should describe the goal as a short, active verb phrase.** |
| --- | --- | --- |
| Brief description | The case addresses the transition from lower secondary school to upper secondary education – one of the most central transitions in the life course of children and young people. The transition involves both a change in everyday school life and a formal transfer of responsibility from municipality to county authority, and affects many actors, services and systems.For young people, this is a phase marked by expectations, choices and increased responsibility for their own everyday lives. For parents and guardians, it is about the reassurance that the child receives the right follow-up. For employees in schools and support services, it is about providing a good offer, often under time pressure and with limited overview.In this transition there is a need for relevant information to follow the pupil in a safe, precise and understandable way – without the pupil or parents and guardians themselves having to act as information carriers between actors. The case sheds light on how current practice and systems only to a limited extent support this need. | Concise description of the use case, including context and scope. Describe what is included and what is outside (the black-box scope). |
| Primary actor | • Pupil (possibly parent or guardian) | The role that initiates the use case and holds the main goal. There shall be only one primary actor. |
| Secondary actors | • Lower secondary school (municipality)• Upper secondary school (county)• PPT/OT• School administration systems | Other roles or systems that support or are affected by the use case. May be users or technical systems. |
| Stakeholders | • Pupil/parent or guardian – safe transition• Municipality/county – correct follow-up• PPT/OT – access to relevant info• Authorities – compliance and quality | Names of stakeholders and their primary interest in the goal the use case describes. There may be several stakeholders. |
| Specific considerations (overall) | Today many people experience that the transition between lower secondary school and upper secondary school is not sufficiently supported by coherent information flow. Important knowledge about the pupil's school career, need for adaptations, previous measures or follow-up is often not available to the right actor at the right time.This means that information must be gathered again or reassessed, and that follow-up may be delayed or inadequate.Breaks occur in particular:when responsibility is transferred from municipality to county authoritywhen different services and levels of government have different understandings of concepts, roles and responsibilitieswhen specialist systems and work processes are not adapted to collaboration across boundarieswhen there is uncertainty about what information can, should and must be sharedFor end users (young people and parents and guardians):Insecurity in an already demanding transitionNeed to explain situation and needs several timesRisk of delayed or inadequate follow-upFor employees in the services:Extra work related to manual coordinationLack of overall overview and uncertainty in decisionsRisk that measures are not continued or come too lateFor the organisations:Inefficient use of time and resourcesIncreased risk of errors, delays and dropout | Particular implications and considerations beyond general legal and architecture requirements, e.g. relating to AI, privacy, security and universal design. |
| Accessibility | • Plain language and universal design• Support for different levels of competence/languages where relevant | Identified considerations relating to universal design and accessibility for different user groups. |
| Generative AI | • Clarify area of use (drafting/classification/decision support)• Human control and verifiability | Identified considerations relating to the use of generative AI, e.g. transparency, verifiability, bias and human control. |
| Diagram | USER FLOW  [Pupil/parent or guardian] -> [Lower secondary school] -> [Transfer/access] -> [Upper secondary school] -> [Follow-up]DATA FLOW  [School admin. (municipality)] -> (standardised transfer) -> [School admin. (county)]  [PPT/OT] <-> (access-controlled sharing) <-> [School] : measures/adaptations (minimised) | Visualisation showing the data flow between actors and system components that enable the use case. Use the recommended symbol set (cf. Appendix C2). |
| Implications for interoperability | Breaks in information flow/responsibility (from source text):Breaks occur in particular:when responsibility is transferred from municipality to county authoritywhen different services and levels of government have different understandings of concepts, roles and responsibilitieswhen specialist systems and work processes are not adapted to collaboration across boundarieswhen there is uncertainty about what information can, should and must be sharedData flows that must be supported: identity/access, core information for the use case, status changes/events, and traceable logging. | Identification of which data flows must be supported, and which interoperability standards should be used where possible. |
| Notes | Source document (step 2): 02 Sømløs overgang grunnskole-videregående.docx | Supplementary notes and references used or mentioned elsewhere in the table. |


### Rationale (analysis) – SAMT-BU-010


*Follow-up of young people at risk of falling outside education and employment*

#### UFO – ontological clarification


This use case concerns a situation where the absence of attachment – to school, work or measures – itself becomes a central characteristic of the individual's situation. Ontologically, the case is not about a single service, but about a **gap** between services, where responsibility is fragmented and often time-limited. The analysis shows that the risk of exclusion arises precisely in this gap, when no actor has overall responsibility for the follow-up.

#### Legal method


From a legal perspective, the use case raises questions about proper follow-up when young people are no longer covered by clear rights or duties related to schooling. When responsibility is distributed between different services with different mandates, uncertainty may arise about who actually has responsibility for following up. The analysis points out that a lack of coordination in such situations can lead to young people being left without any offer, despite the need for follow-up being obvious.

#### Toulmin – implicit argumentation


The implicit claim in the use case is that the risk of lasting exclusion increases when follow-up is fragmented and without clear ownership. The grounds for this claim lie in the description of young people who fall between schemes and measures. The qualifications concern the fact that follow-up must be adapted to the individual's situation and not be standardised in a way that overlooks individual needs. The case thus argues for better coordination, not for more isolated measures.

#### SWOT – strategic assessment


The strength of this use case is that it focuses on a group where early and coordinated efforts can have a great effect. The weakness lies in current responsibility often being divided between several actors without a shared overview. The opportunity lies in establishing clear lines of responsibility and coherent follow-up, while the threat is that a lack of collaboration leads to long-term exclusion with major consequences for society.

#### iStar – goals and dependencies


The analysis reveals that different services depend on each other to be able to provide effective follow-up, while the young person depends on someone actually taking responsibility for the whole. When this dependency is not explicitly handled, follow-up becomes random and dependent on individuals. The use case points to the need to clarify both goals and responsibilities in the follow-up of young people in the risk zone.

#### TOGAF / ArchiMate – architecture implications


The architecture implication of the use case is that follow-up of young people at risk requires mechanisms that provide an overview of status, measures and responsibility across services. This points to the need for support for coordination and information sharing that can work even when young people move between different schemes. Such an architecture reduces the risk of responsibility «disappearing» in the transitions.

#### KF extended NIF/EIF – interoperability


The use case shows that interoperability in the follow-up of young people outside education and employment depends on both organisational cooperation and a shared understanding of goals. Technology can support overview and coordination, but without shared prioritisation and competence, the measures will remain fragmented. The analysis therefore points to the need for coordinated efforts across services, both professionally and organisationally.

#### Brief assessment


SAMT-BU-010 makes clear that the risk of exclusion often arises where responsibility is unclear and follow-up fragmented. The case shows that coherent services presuppose clear roles, coordinated efforts and structures that make it possible to follow up young people even when they find themselves between established schemes.

## SAMT-BU-011 – Digital dialogue and increased involvement between kindergarten/school and the home (parents and guardians, and pupils).


| **ID and title of ****use****-****case** | **SAMT-BU-011 – Digital dialogue and increased involvement between kindergarten/school and the home (parents and guardians, and pupils).** | **Unique local identifier and title for the ****use case****. The title should describe the goal as a short, active verb phrase.** |
| --- | --- | --- |
| Brief description | The use case concerns: Digital dialogue and increased involvement between kindergarten/school and the home (parents and guardians, and pupils).. (Based on the case register.) | Concise description of the use case, including context and scope. Describe what is included and what is outside (the black-box scope). |
| Primary actor | (to be clarified) | The role that initiates the use case and holds the main goal. There shall be only one primary actor. |
| Secondary actors | • (to be clarified) | Other roles or systems that support or are affected by the use case. May be users or technical systems. |
| Stakeholders | • (to be clarified) | Names of stakeholders and their primary interest in the goal the use case describes. There may be several stakeholders. |
| Specific considerations (overall) | To be clarified. | Particular implications and considerations beyond general legal and architecture requirements, e.g. relating to AI, privacy, security and universal design. |
| Accessibility | • (to be clarified)• (to be clarified) | Identified considerations relating to universal design and accessibility for different user groups. |
| Generative AI | • (to be clarified)• (to be clarified) | Identified considerations relating to the use of generative AI, e.g. transparency, verifiability, bias and human control. |
| Diagram | USER FLOW (conceptual)  [End user] --> [Service/Front end] --> [Caseworker/Adviser] --> [Decision/Follow-up]DATA FLOW (conceptual)  [Client/portal] -> [Specialist system A] -> (API/Event) -> [Specialist system B] -> [Reporting/Log] | Visualisation showing the data flow between actors and system components that enable the use case. Use the recommended symbol set (cf. Appendix C2). |
| Implications for interoperability | To be clarified. | Identification of which data flows must be supported, and which interoperability standards should be used where possible. |
| Notes | (no notes in the case register) | Supplementary notes and references used or mentioned elsewhere in the table. |


### Rationale (analysis) – SAMT-BU-011


*Coordinated collaboration with parents and guardians around children and young people*

#### UFO – ontological clarification


This use case makes clear that parents and guardians are not merely supporters, but **actors with their own roles and rights** in the service pathway around children and young people. Ontologically, the case concerns the relationship between children, parents and guardians, and public services, where responsibility and decision-making authority are shared and often time-limited. The analysis shows that the challenge does not lie in a lack of involvement of parents and guardians, but in a lack of clarity about **how and when** parents and guardians are to take part in service delivery.

#### Legal method


Legally, the use case touches on central questions of parental responsibility, representation and the child's right to participation. When several services are involved, uncertainty may arise as to which information parents and guardians are entitled to, and which information should be communicated directly to the child or young person. The analysis points out that a lack of shared practice may lead either to over-involvement or to exclusion of parents and guardians, both with potential consequences for legal certainty.

#### Toulmin – implicit argumentation


The implicit claim in the use case is that the quality of follow-up is strengthened when parents and guardians are involved in a clear and predictable way. The grounds for this claim lie in the description of misunderstandings and lack of coordination when parents and guardians do not have a clear role. The qualifications concern the child's age, maturity and right to self-determination. The case therefore argues for differentiated and situation-adapted involvement, not for standardised practice.

**SWOT – strategic assessment**

The strength of this use case is that parents and guardians often possess important contextual knowledge and can contribute to better follow-up. The weakness lies in the fact that roles and expectations are often unclarified between services. The opportunity lies in establishing clear frameworks for collaboration with parents and guardians that can be used across services, while the threat is that a lack of clarification creates conflicts and weakens trust between the parties.

**iStar**** – goals and dependencies**

The analysis makes visible that both services and parents and guardians are mutually dependent on clear communication and clarification of roles. At the same time, the child depends on the collaboration taking place in a way that safeguards both support and independence. The use case points out that when these dependencies are not handled explicitly, the collaboration can become person-dependent and inconsistent.

#### TOGAF / ArchiMate – architecture implications


The architecture implication of the use case is that collaboration with parents and guardians must be supported by structures that handle access, communication and consent in a controlled manner. This points to the need for shared mechanisms that can be adapted to the child's age and situation, and that can be used across services without creating information leaks or misunderstandings.

#### KF extended NIF/EIF – interoperability


The use case shows that interoperability with parents and guardians depends to a large extent on competence in both regulations and communication. Technological solutions can support structure and overview, but without a shared understanding of roles and responsibilities the effect will be limited. The analysis therefore points to the need for both competence development and clear governance of practice for collaboration with parents and guardians.

#### Brief assessment


SAMT-BU-011 shows that parents and guardians are a central part of coherent services for children and young people. The case makes clear that quality in follow-up presupposes clear frameworks for involvement, in which both the child's rights and the role of parents and guardians are safeguarded in a balanced and predictable manner.

## SAMT-BU-012 – Change of educational pathway or programme of study.


| **ID and title of ****use****-****case** | **SAMT-BU-012 – Change of educational pathway or programme of study.** | **Unique local identifier and title for the ****use case****. The title should describe the goal as a short, active verb phrase.** |
| --- | --- | --- |
| Brief description | The use case concerns: Change of educational pathway or programme of study.. (Based on the case register.) | Concise description of the use case, including context and scope. Describe what is included and what is outside (the black-box scope). |
| Primary actor | (to be clarified) | The role that initiates the use case and holds the main goal. There shall be only one primary actor. |
| Secondary actors | • (to be clarified) | Other roles or systems that support or are affected by the use case. May be users or technical systems. |
| Stakeholders | • (to be clarified) | Names of stakeholders and their primary interest in the goal the use case describes. There may be several stakeholders. |
| Specific considerations (overall) | To be clarified. | Particular implications and considerations beyond general legal and architecture requirements, e.g. relating to AI, privacy, security and universal design. |
| Accessibility | • (to be clarified)• (to be clarified) | Identified considerations relating to universal design and accessibility for different user groups. |
| Generative AI | • (to be clarified)• (to be clarified) | Identified considerations relating to the use of generative AI, e.g. transparency, verifiability, bias and human control. |
| Diagram | USER FLOW (conceptual)  [End user] --> [Service/Front end] --> [Caseworker/Adviser] --> [Decision/Follow-up]DATA FLOW (conceptual)  [Client/portal] -> [Specialist system A] -> (API/Event) -> [Specialist system B] -> [Reporting/Log] | Visualisation showing the data flow between actors and system components that enable the use case. Use the recommended symbol set (cf. Appendix C2). |
| Implications for interoperability | To be clarified. | Identification of which data flows must be supported, and which interoperability standards should be used where possible. |
| Notes | (no notes in the case register) | Supplementary notes and references used or mentioned elsewhere in the table. |


### Rationale (analysis) – SAMT-BU-012


*Coordinated handling of consent and the right to opt out for children and young people*

#### UFO – ontological clarification


This use case makes clear that consent and opting out are not static events, but **situation- and time-dependent relationships** between person, information and service. Ontologically, the case concerns how will, maturity and legal capacity develop over time, and how this affects who can make decisions on behalf of the child or young person. The analysis shows that the challenge is not a lack of consent, but a lack of structure for handling changes in capacity to consent and in preferences across services.

#### Legal method


Legally, the use case touches on core principles such as the best interests of the child, participation and the right to privacy. When several services relate to different consents and opt-outs, inconsistency easily arises in practice. The analysis points out that current solutions often handle consent in isolation per service, which increases the risk of both oversharing and unjustified restriction of information. The case therefore points to the need for more holistic and verifiable handling of consent over time.

#### Toulmin – implicit argumentation


The implicit claim in the use case is that legal certainty is strengthened when consent is handled consistently and comprehensibly for everyone involved. The grounds for this claim lie in the description of uncertainty and manual handling in current practice. The qualifications relate to the fact that consent must always be voluntary, informed and possible to withdraw. The case therefore argues for structure and overview, not for standardisation that reduces individual assessment.

**SWOT – strategic assessment**

The strength of this use case is that better consent handling can bring increased trust between citizens and services. The weakness lies in the complexity related to age, maturity and varying regulations. The opportunity lies in establishing shared understanding and support for handling consent across services, while the threat is that unclear solutions lead to breaches of rights or loss of trust.

#### iStar – goals and dependencies


The analysis makes visible that services depend on correct information about consent status in order to act correctly. At the same time, the child and young person depend on their will actually being respected and enforced in practice. The use case points out that when these dependencies are not supported by shared structures, the handling of consent becomes person-dependent and unpredictable.

#### TOGAF / ArchiMate – architecture implications


The architecture implication of the use case is that consent and opting out should be treated as separate information objects with a life cycle, not as attributes scattered across different systems. This points to the need for shared mechanisms that can expose consent status in a controlled manner, while details and context remain where they belong. Such an architecture supports both precision and verifiability.

#### KF extended NIF/EIF – interoperability


The use case shows that interoperability around consent requires a high level of competence in both regulations and ethics. Technology can support overview and consistency, but without a shared understanding of principles and responsibilities the solutions will lose legitimacy. The analysis therefore points to the need for coordinated competence development and clear management of consent solutions across services.

#### Brief assessment


SAMT-BU-012 shows that consent is a fundamental prerequisite for coherent services, not an administrative add-on. The case makes clear that holistic and verifiable handling of consent is crucial for safeguarding rights, trust and quality in service delivery.

.

## SAMT-BU-013 – Interrupted education (dropout).


| **ID and title of ****use****-****case** | **SAMT-BU-013 – Interrupted education (dropout).** | **Unique local identifier and title for the ****use case****. The title should describe the goal as a short, active verb phrase.** |
| --- | --- | --- |
| Brief description | The use case concerns: Interrupted education (dropout).. (Based on the case register.) | Concise description of the use case, including context and scope. Describe what is included and what is outside (the black-box scope). |
| Primary actor | (to be clarified) | The role that initiates the use case and holds the main goal. There shall be only one primary actor. |
| Secondary actors | • (to be clarified) | Other roles or systems that support or are affected by the use case. May be users or technical systems. |
| Stakeholders | • (to be clarified) | Names of stakeholders and their primary interest in the goal the use case describes. There may be several stakeholders. |
| Specific considerations (overall) | To be clarified. | Particular implications and considerations beyond general legal and architecture requirements, e.g. relating to AI, privacy, security and universal design. |
| Accessibility | • (to be clarified)• (to be clarified) | Identified considerations relating to universal design and accessibility for different user groups. |
| Generative AI | • (to be clarified)• (to be clarified) | Identified considerations relating to the use of generative AI, e.g. transparency, verifiability, bias and human control. |
| Diagram | USER FLOW (conceptual)  [End user] --> [Service/Front end] --> [Caseworker/Adviser] --> [Decision/Follow-up]DATA FLOW (conceptual)  [Client/portal] -> [Specialist system A] -> (API/Event) -> [Specialist system B] -> [Reporting/Log] | Visualisation showing the data flow between actors and system components that enable the use case. Use the recommended symbol set (cf. Appendix C2). |
| Implications for interoperability | To be clarified. | Identification of which data flows must be supported, and which interoperability standards should be used where possible. |
| Notes | (no notes in the case register) | Supplementary notes and references used or mentioned elsewhere in the table. |


### Rationale (analysis) – SAMT-BU-013


*Sharing of relevant information when moving between municipalities*

#### UFO – ontological clarification


This use case makes visible an ontological break that occurs when **organisational boundaries change**, while the person remains the same. Moving between municipalities does not in itself entail a new service need, but a transition in administrative responsibility. Ontologically, the case therefore concerns continuity in the relationship between the individual and services, despite a change in organisational context. The challenge lies in the fact that information is often closely tied to the municipality as an organisational unit, rather than to the person as the bearer of information.

#### Legal method


Legally, the use case raises questions about transfer of responsibility, duty to inform and purpose limitation. When one municipality ends its responsibility and another takes over, a grey zone arises in which relevant information risks falling between the cracks. The analysis points out that a lack of structured information sharing may lead to new services starting follow-up without the necessary context, while at the same time unnecessary information must not be transferred. The case thus points to the need for precise and needs-based sharing when moving.

#### Toulmin – implicit argumentation


The implicit claim in the use case is that the quality of follow-up is weakened when moving entails a break in information. The grounds for this claim lie in the description of loss of history and failure to carry forward assessments. The qualifications concern the risk of oversharing and lack of legal basis. The case therefore argues for structured handover of relevant information, not for general transfer of entire case histories.

#### SWOT – strategic assessment


The strength of this use case is that the benefit of better information flow when moving is clear: faster and more targeted follow-up in the new municipality. The weakness lies in current practice, where handover is often person-dependent or inadequate. The opportunity lies in establishing shared mechanisms for transition between municipalities, while the threat is that differing practice and interpretation of regulations lead to unpredictability for the child and the family.

#### iStar – goals and dependencies


The analysis makes visible that both the transferring and the receiving municipality depend on information being transferred in a controlled manner. The child and the family, at the same time, depend on not having to repeat their history and needs. The use case points out that when these dependencies are not supported by shared structures, the transition becomes burdensome and inefficient.

#### TOGAF / ArchiMate – architecture implications


The architecture implication of the use case is that information sharing when moving must be supported by standardised processes and information objects that can be used across municipalities. This points to the need for shared architecture principles that ensure continuity without creating centralisation of data. Such an approach gives better control and predictability in the transitions.

#### KF extended NIF/EIF – interoperability


The use case shows that interoperability when moving depends on both legal and organisational maturity across municipalities. Technology can support transfer, but without a shared understanding of responsibility and purpose, practice will vary. The analysis therefore points to the need for a coordinated understanding of regulations, competence and funding for solutions that support transition between municipalities.

#### Brief assessment


SAMT-BU-013 makes clear that moving between municipalities is a critical point for coherent services. The case shows that quality in follow-up presupposes structures that safeguard continuity of information and responsibility, without compromising privacy and legal certainty.

## SAMT-BU-014 – Documentation and sharing of diplomas and certificates of competence.


| **ID and title of ****use****-****case** | **SAMT-BU-014 – Documentation and sharing of diplomas and certificates of competence.** | **Unique local identifier and title for the ****use case****. The title should describe the goal as a short, active verb phrase.** |
| --- | --- | --- |
| Brief description | The case addresses how results from upper secondary education can be made available in a better and more coherent way to actors who need the information in the further follow-up of young people. Results may, for example, be the status of completed education, completion, competence, assessments or documentation of the level achieved.The situation in focus is the transition from upper secondary education to the next phase in young people's life course, such as further education, work or follow-up services. In this phase it is crucial that relevant information is available at the right time, in the right form and for the right actor.Today it is often the young people themselves who must help communicate or document their own status. The case highlights how current practice and systems only to a limited extent support holistic availability and reuse of results information across services and levels of government. | Concise description of the use case, including context and scope. Describe what is included and what is outside (the black-box scope). |
| Primary actor | • Young person completing upper secondary | The role that initiates the use case and holds the main goal. There shall be only one primary actor. |
| Secondary actors | • Upper secondary school/county authority• Follow-up services/NAV/higher education (where relevant)• School administration/competence systems | Other roles or systems that support or are affected by the use case. May be users or technical systems. |
| Stakeholders | • Young people – easy access to status/competence• Advisers – basis for decisions• Organisations – efficient use of resources• Directorate/ministry – frameworks/reporting | Names of stakeholders and their primary interest in the goal the use case describes. There may be several stakeholders. |
| Specific considerations (overall) | Today, information about results from upper secondary education is often spread across several systems and available in different formats. It is not always clear who has access to which information, when the information is available, or how it can be used further.This means that:information must be obtained manually or anewemployees lack an overview in guidance and follow-up workyoung people themselves must explain or document their own status several timesBreaks in information flow and responsibility occur in particular:when young people move on to work, higher education or follow-up serviceswhen different actors need the same information, but for different purposeswhen it is unclear who is responsible for making information availablewhen systems and work processes do not support reuse of existing dataFor young peopleLack of overview of their own status and competenceNeed to document or explain their own situation several timesRisk of delayed or inadequate guidance and follow-upFor employees in the servicesAdditional work related to manual collection and checking of informationUncertainty in the basis for decisions on guidance and follow-upRisk of errors or misunderstandings relating to results and competenceFor the organisationsInefficient use of time and resourcesFailure to make use of information that already existsReduced quality and consistency in the data basis | Particular implications and considerations beyond general legal and architecture requirements, e.g. relating to AI, privacy, security and universal design. |
| Accessibility | • Plain language and universal design• Support for different competence levels/languages where relevant | Identified considerations relating to universal design and accessibility for different user groups. |
| Generative AI | • Clarify area of use (drafts/classification/decision support)• Human control and verifiability | Identified considerations relating to the use of generative AI, e.g. transparency, verifiability, bias and human control. |
| Diagram | USER FLOW  [Young person] -> [Upper secondary school] -> [Access to results] -> [Further education/work/OT]DATA FLOW  [School admin./competence system] -> (API) -> [Results service/portal]  [Results service] -> (role-/purpose-based access) -> [NAV/OT/higher education] | Visualisation showing the data flow between actors and system components that enable the use case. Use the recommended symbol set (cf. Appendix C2). |
| Implications for interoperability | Breaks in information flow/responsibility (from source text):Breaks in information flow and responsibility occur in particular:when young people move on to work, higher education or follow-up serviceswhen different actors need the same information, but for different purposeswhen it is unclear who is responsible for making information availablewhen systems and work processes do not support reuse of existing dataData flows that must be supported: identity/access, core information for the use case, status changes/events, and traceable logging. | Identification of which data flows must be supported, and which interoperability standards should be used where possible. |
| Notes | Source document (step 2): 01 Kunnskapsoversikt.docx | Supplementary notes and references used or mentioned elsewhere in the table. |


### Rationale (analysis) – SAMT-BU-014


*Coordinated follow-up in the transition from youth to adult services*

#### UFO – ontological clarification


This use case makes visible a fundamental ontological shift: the individual goes from being a **young person under special arrangements** to becoming an **adult with ordinary rights and obligations**. Ontologically, the case concerns continuity in needs and life situation, while the service context changes significantly. The analysis shows that the challenge does not lie in the needs ceasing at the age of majority, but in the services around the individual often being structured as if they do.

#### Legal method


Legally, the use case raises the transition from special rules for children and young people to adult regulations, in which rights, obligations and responsibilities all change. The analysis points out that a lack of coordination in this transition may lead to the young person losing adapted services without being prepared for new requirements. The case therefore points to the need for clear transition processes that safeguard both legal certainty and proper follow-up when responsibility moves between regulatory regimes.

#### Toulmin – implicit argumentation


The implicit claim in the use case is that the risk of exclusion and breaks in follow-up increases when the transition to adult services takes place without coordination. The grounds for this claim lie in the description of young people losing support in the transition phase. The qualifications concern the fact that adult services cannot fully mirror youth services. The case therefore argues for a planned and gradual transition, not for continuation of the same measures.

#### SWOT – strategic assessment


The strength of this use case is that the transition to adult services is a predictable point in time that can be planned for. The weakness lies in responsibility often being shared between several services without a joint plan. The opportunity lies in establishing structured transition pathways that can be used for many young people, while the threat is that a lack of coordination leads to loss of follow-up in a critical phase.

#### iStar – goals and dependencies


The analysis makes visible that young people depend on the transition being handled in a way that provides predictability and support. At the same time, adult services depend on receiving relevant insight in order to take over responsibility in a proper manner. The use case points out that when these dependencies are not explicitly handled, the transition becomes person-dependent and uneven.

#### TOGAF / ArchiMate – architecture implications


The architecture implication of the use case is that the transition to adult services must be supported by processes and information structures that clearly mark the shift in responsibility. This points to the need for shared transition mechanisms and information objects that can be used across services. Such an architecture gives better traceability and reduces the risk of breaks in follow-up.

#### KF extended NIF/EIF – interoperability


The use case shows that interoperability in the transition to adult services requires a high degree of organisational maturity. Technology can support planning and handover, but without clear clarification of roles and competence the transition will remain vulnerable. The analysis therefore points to the need for both competence development and binding governance of transition processes.

#### Brief assessment


SAMT-BU-014 makes clear that the age of majority does not mark an end point for needs, but a shift in frameworks. The case shows that coherent services presuppose planned transitions in which responsibility, information and expectations are adjusted in a controlled and predictable manner.

## SAMT-BU-015 – Procurement of specialist and support systems – a greater degree of shared approach / procurement of specialist systems through defined frameworks, models and architecture


| **ID and title of ****use****-****case** | **SAMT-BU-015 – Procurement of specialist and support systems – a greater degree of shared approach / procurement of specialist systems through defined frameworks, models and architecture** | **Unique local identifier and title for the ****use case****. The title should describe the goal as a short, active verb phrase.** |
| --- | --- | --- |
| Brief description | The use case concerns: Procurement of specialist and support systems – a greater degree of shared approach / procurement of specialist systems through defined frameworks, models and architecture. (Based on the case register.) | Concise description of the use case, including context and scope. Describe what is included and what is outside (the black-box scope). |
| Primary actor | (to be clarified) | The role that initiates the use case and holds the main goal. There shall be only one primary actor. |
| Secondary actors | • (to be clarified) | Other roles or systems that support or are affected by the use case. May be users or technical systems. |
| Stakeholders | • (to be clarified) | Names of stakeholders and their primary interest in the goal the use case describes. There may be several stakeholders. |
| Specific considerations (overall) | To be clarified. | Particular implications and considerations beyond general legal and architecture requirements, e.g. relating to AI, privacy, security and universal design. |
| Accessibility | • (to be clarified)• (to be clarified) | Identified considerations relating to universal design and accessibility for different user groups. |
| Generative AI | • (to be clarified)• (to be clarified) | Identified considerations relating to the use of generative AI, e.g. transparency, verifiability, bias and human control. |
| Diagram | USER FLOW (conceptual)  [End user] --> [Service/Front end] --> [Caseworker/Adviser] --> [Decision/Follow-up]DATA FLOW (conceptual)  [Client/portal] -> [Specialist system A] -> (API/Event) -> [Specialist system B] -> [Reporting/Log] | Visualisation showing the data flow between actors and system components that enable the use case. Use the recommended symbol set (cf. Appendix C2). |
| Implications for interoperability | To be clarified. | Identification of which data flows must be supported, and which interoperability standards should be used where possible. |
| Notes | (no notes in the case register) | Supplementary notes and references used or mentioned elsewhere in the table. |


### Rationale (analysis) – SAMT-BU-015


*Coordinated information sharing in crises and acute situations concerning children and young people*

#### UFO – ontological clarification


This use case concerns situations where **time becomes a critical factor**, and where normal ways of working are challenged by the need for rapid action. Ontologically, the case is about temporary states of high severity, in which relationships between actors intensify and decisions must be made under uncertainty. The analysis shows that the challenge is not a lack of information, but the need to quickly establish a shared situational picture without breaching fundamental principles of responsibility and rights.

#### Legal method


From a legal perspective, the use case brings to the fore assessments resembling those of necessity, where consideration for the child's safety may weigh heavily, while requirements for documentation and verifiability remain. The analysis points out that unclear frameworks in acute situations often lead either to excessive caution or to informal practice. The case therefore points to the need for clear guidelines that support correct legal assessments even when decisions must be made quickly.

#### Toulmin – implicit argumentation


The implicit claim in the use case is that rapid and coordinated information sharing can be decisive in averting harm. The grounds for this claim lie in the description of situations where delay has serious consequences. The qualifications concern the risk of misjudgements under pressure. The case therefore argues for pre-agreed frameworks for information sharing in crises, not for improvised solutions.

#### SWOT – strategic assessment


The strength of this use case is that the need for rapid collaboration is clear and widely understood. The weakness lies in the fact that crisis situations often reveal shortcomings in routines and collaboration that are otherwise hidden. The opportunity lies in using experience from crises to strengthen ordinary collaboration mechanisms, while the threat is that lack of preparation leads to mishandling at critical moments.

#### iStar – goals and dependencies


The analysis shows that actors in crisis situations are strongly interdependent on each other's information and assessments. At the same time, the child and the family depend on decisions being made quickly, but correctly. The use case points out that when these dependencies are not explicitly supported, the risk of both wrong decisions and subsequent questions of accountability increases.

#### TOGAF / ArchiMate – architecture implications


The architecture implication of the use case is that collaboration in crises must be supported by structures that remain robust under pressure. This points to the need for clear process flows, defined information objects and mechanisms for traceability, so that both action and documentation can take place in parallel. Such an architecture reduces reliance on improvisation.

#### KF extended NIF/EIF – interoperability


The use case shows that interoperability in crises requires a high level of maturity across the legal, organisational and technical dimensions. Technology can support rapid access to information, but without a shared understanding of roles and responsibilities the effect will be limited. The analysis therefore points to the need for regular exercises, competence building and clear governance of collaboration practice in crisis situations.

#### Brief assessment


SAMT-BU-015 makes clear that crises put interoperability to the test. The case shows that coherent services require frameworks for information sharing and coordination to be clarified in advance, so that the best interests of the child can be safeguarded even when the situation is acute and complex.

## SAMT-BU-016 – AI solutions based on structured, shared information models within childhood and education, in collaboration with other AI initiatives.


| **ID and title of ****use****-****case** | **SAMT-BU-016 – AI solutions based on structured, shared information models within childhood and education, in collaboration with other AI initiatives.** | **Unique local identifier and title for the ****use case****. The title should describe the goal as a short, active verb phrase.** |
| --- | --- | --- |
| Brief description | ID management of refugees and asylum seekersChange of IDSafeguarding the person's data and rights when changing ID number | Concise description of the use case, including context and scope. Describe what is included and what is outside (the black-box scope). |
| Primary actor | • Employee in a municipal service (caseworker/registrar) | The role that initiates the use case and holds the main goal. There shall be only one primary actor. |
| Secondary actors | • National Population Register/FIKS (identity service)• Municipal specialist systems• Integration platform | Other roles or systems that support or are affected by the use case. May be users or technical systems. |
| Stakeholders | • Children/young people/parents and guardians – access and rights• The municipality – correct case processing, data quality• System suppliers – support for ID change• Government actors – identity management | Names of stakeholders and their primary interest in the goal the use case describes. There may be several stakeholders. |
| Specific considerations (overall) | Within childhood and education there is no shared solution for assigning ID numbers to persons who have not yet received a D-number or F-number in the National Population Register. As a rule, parents receive a D-number in connection with having to pay tax, while it may take longer before children receive a D-number or national identity number. Pending this, the municipalities must register a number of fictitious national identity numbers according to their own arrangements. The person objects thus potentially arise with a number of different identifiers across the public sector.The municipalities provide services to persons who are not registered in the National Population Register with a D-number or F-number. Municipalities are thereby forced, each in their own sectors, to create one or many fictitious versions of these person objects pending these persons receiving an ID number in the National Population Register. There is no coordination of such fictitious numbers between sectors or between the various municipalities and county authorities.End users;children, young people, parents and guardians,Employees in the «services»Specialist system suppliersPremise setters: interest organisation, directorate, ministry and any othersHow are the actors affected by the current situation, and what are the possible consequencesBecause each individual municipality, or public body, has a duty and a self-interest in keeping track of person objects in the various IT systems, the administration spends a good deal of time manually linking registered children to the new, correct person objects after parents have typically received a D-number or F-number before their children. This is time-consuming and may cause uncertainty.The municipalities have a duty to provide persons with a number of services, such as a kindergarten place and a school place, even if they have no ID in the National Population Register.When persons eventually receive an ID number in the National Population Register, there is nothing automatic that allows the municipality to say with certainty that new person objects imported from the National Population Register are with 100% certainty the same as those the municipality has registered in the various systems with a fictitious number. Only similarity in name and address can give a degree of indication of this. In the worst case, errors may occur. It is somewhat easier when the child eventually receives a D-number or national identity number, because the parent relationships then usually also follow in the data flow from the National Population Register. Unfortunately, this often happens long after the parents receive such a number in the National Population Register.Many systems support the transition from D-number to F-number in that the integration provides information about the change. This makes it possible to automate the change, and thereby potentially ensures that data is not lost or made inaccessible.The ID number is usually the primary key for person objects. So without automation or good control, duplicates of person objects will typically arise in several systems. This may mean that information is not found, such as decisions, or that parents or pupils lose data they have stored in various IT systems.Fictitious numbers also do not give access to log in to public IT systems with ID-porten.Health has come further with a shared solution here, as I understand it, and has something called Hjelpenummer. Read more about it here, as well as the challenges they describe, which can well be compared with other public sectors:https://www.nrk.no/norge/darlig-id-system-en-pasientfare-1.11425318 | Particular implications and considerations beyond general legal and architecture requirements, e.g. relating to AI, privacy, security and universal design. |
| Accessibility | • Plain language and universal design• Support for different competence levels/languages where relevant | Identified considerations relating to universal design and accessibility for different user groups. |
| Generative AI | • Clarify area of use (drafts/classification/decision support)• Human control and verifiability | Identified considerations relating to the use of generative AI, e.g. transparency, verifiability, bias and human control. |
| Diagram | USER FLOW  [Parent or guardian/child] -> [Municipal service] -> [Registration in specialist system] -> [Update on new ID]DATA FLOW  [Specialist systems in municipality] <-> [National Population Register/FIKS] : identities/status changes  [Specialist system] -> [Integration layer] -> [Other specialist systems] : ID change (D->F) + linking | Visualisation showing the data flow between actors and system components that enable the use case. Use the recommended symbol set (cf. Appendix C2). |
| Implications for interoperability | Breaks in information flow/responsibility (from source text):The municipalities provide services to persons who are not registered in the National Population Register with a D-number or F-number. Municipalities are thereby forced, each in their own sectors, to create one or many fictitious versions of these person objects pending these persons receiving an ID number in the National Population Register. There is no coordination of such fictitious numbers between sectors or between the various municipalities and county authorities.Data flows that must be supported: identity/access, core information for the use case, status changes/events, and traceable logging. | Identification of which data flows must be supported, and which interoperability standards should be used where possible. |
| Notes | Source document (step 2): 03 Case-håndtering av Dnr-v0.9.docx | Supplementary notes and references used or mentioned elsewhere in the table. |


### Rationale (analysis) – SAMT-BU-016


*Transfer of responsibility and information when changing service provider within the same municipality*

#### UFO – ontological clarification


This use case highlights an ontological shift in which **the role of responsible service provider changes**, while both the person and the need remain. Ontologically, the case is about continuity in service delivery when organisational or internal structures change, for example when changing department, team or caseworker. The analysis shows that the challenge does not lie in a lack of information, but in the lack of explicit transfer of responsibility and context when responsibility is moved internally.

#### Legal method


From a legal perspective, the use case raises questions of sound case processing and documentation. When responsibility changes internally, it is crucial that relevant assessments, decisions and reasons accompany it, so that the new service provider can continue the follow-up on a correct basis. The analysis points out that inadequate internal transfer can lead to both misjudgements and breaks in continuity, even though the service is formally the same.

#### Toulmin – implicit argumentation


The implicit claim in the use case is that the quality of follow-up is weakened when responsibility is transferred without a structured flow of information. The grounds for this claim lie in the description of loss of context in internal transitions. The qualifications concern the fact that not all information is necessarily relevant to carry forward. The case therefore argues for selective and purpose-driven transfer of information, not for full copying of the case history.

#### SWOT – strategic assessment


The strength of this use case is that improvements can yield rapid benefits, because transitions happen often and are predictable. The weakness lies in the fact that internal collaboration is often taken for granted and therefore lacks clear structures. The opportunity lies in establishing a shared practice for internal handover, while the threat is that person-dependent solutions lead to varying quality in follow-up.

#### iStar – goals and dependencies


The analysis shows that the new service provider depends on gaining sufficient insight to be able to take over responsibility safely. At the same time, the child and the family depend on the transition not being experienced as a break. The use case points out that when these dependencies are not supported by clear routines, the risk of misunderstandings and delays increases.

#### TOGAF / ArchiMate – architecture implications


The architecture implication of the use case is that internal transitions should be supported by processes and information structures that clearly mark the change of responsibility. This points to the need for mechanisms that can transfer status, assessments and ongoing measures without losing traceability. Such an architecture strengthens both efficiency and quality in service delivery.

#### KF extended NIF/EIF – interoperability


The use case shows that interoperability is also critical internally within the organisation. Technology can support the transfer of information, but without a shared understanding of responsibility and practice the effect will be limited. The analysis therefore points to the need for both organisational anchoring and competence development relating to internal transitions.

#### Brief assessment


SAMT-BU-016 makes clear that coherent services are challenged not only by external boundaries, but also by internal changes in responsibility. The case shows that structured transfer of responsibility and information is crucial to ensuring continuity and quality in follow-up.

## SAMT-BU-017 – Event-driven and automated reporting with an MVP for a new solution for this (e.g. reporting to SSB/KOSTRA)


| **ID and title of ****use****-****case** | **SAMT-BU-017 – Event-driven and automated reporting with an MVP for a new solution for this (e.g. reporting to SSB/KOSTRA)** | **Unique local identifier and title for the ****use case****. The title should describe the goal as a short, active verb phrase.** |
| --- | --- | --- |
| Brief description | The use case concerns: Event-driven and automated reporting with an MVP for a new solution for this (e.g. reporting to SSB/KOSTRA). (Based on the case register.) | Concise description of the use case, including context and scope. Describe what is included and what is outside (the black-box scope). |
| Primary actor | (to be clarified) | The role that initiates the use case and holds the main goal. There shall be only one primary actor. |
| Secondary actors | • (to be clarified) | Other roles or systems that support or are affected by the use case. May be users or technical systems. |
| Stakeholders | • (to be clarified) | Names of stakeholders and their primary interest in the goal the use case describes. There may be several stakeholders. |
| Specific considerations (overall) | To be clarified. | Particular implications and considerations beyond general legal and architecture requirements, e.g. relating to AI, privacy, security and universal design. |
| Accessibility | • (to be clarified)• (to be clarified) | Identified considerations relating to universal design and accessibility for different user groups. |
| Generative AI | • (to be clarified)• (to be clarified) | Identified considerations relating to the use of generative AI, e.g. transparency, verifiability, bias and human control. |
| Diagram | USER FLOW (conceptual)  [End user] --> [Service/Front end] --> [Caseworker/Adviser] --> [Decision/Follow-up]DATA FLOW (conceptual)  [Client/portal] -> [Specialist system A] -> (API/Event) -> [Specialist system B] -> [Reporting/Log] | Visualisation showing the data flow between actors and system components that enable the use case. Use the recommended symbol set (cf. Appendix C2). |
| Implications for interoperability | To be clarified. | Identification of which data flows must be supported, and which interoperability standards should be used where possible. |
| Notes | (no notes in the case register) | Supplementary notes and references used or mentioned elsewhere in the table. |


### Rationale (analysis) – SAMT-BU-017


*Coordinated use of shared concepts and information models across services*

#### UFO – ontological clarification


This use case focuses on a fundamental ontological problem: when different services use **the same word for different phenomena**, or different words for the same phenomenon, the precondition for meaningful collaboration breaks down. Ontologically, the case is about establishing stable and shared concepts for central entities such as child, measure, status, follow-up and responsibility. The analysis shows that the lack of a shared understanding of concepts causes information to lose precision when it moves between services.

#### Legal method


From a legal perspective, the use of concepts has a direct bearing on the application of law. When the same concept is interpreted differently in different services, the risk of divergent practice and wrong decisions increases. The analysis points out that unclear or inconsistent concepts can weaken legal certainty, because it becomes difficult to verify what has actually been assessed and decided. The case therefore points to the need for precise and consistent concepts that can be used across services and regulatory areas.

#### Toulmin – implicit argumentation


The implicit claim in the use case is that the quality of collaboration improves when actors share a common understanding of concepts. The grounds for this claim lie in the description of misunderstandings and the need for manual clarification in current practice. The qualifications concern the fact that concepts must be flexible enough to cover different professional perspectives. The case therefore argues for shared core concepts, not for standardisation of professional practice.

#### SWOT – strategic assessment


The strength of this use case is that shared concepts yield benefits across many other use cases. The weakness lies in the fact that conceptual work is often underestimated and deprioritised. The opportunity lies in establishing concept models that can be reused and further developed over time, while the threat is that lack of management causes the concepts gradually to drift apart again.

#### iStar – goals and dependencies


The analysis shows that all services depend on others interpreting information in the same way as they do themselves. At the same time, the child and the family depend on a consistent understanding in order to encounter predictable practice. The use case points out that when this dependency is not supported by a shared conceptual apparatus, the need for manual coordination and explanation increases.

#### TOGAF / ArchiMate – architecture implications


The architecture implication of the use case is that concepts and information models must be treated as architecture artefacts in their own right, not as implicit assumptions in each system. This points to the need for shared semantic models that can be used across applications and processes. Such an architecture strengthens both interoperability and the capacity for change.

#### KF extended NIF/EIF – interoperability


The use case shows that semantic interoperability is a precondition for all other interoperability. Technology can support the sharing of data, but without shared concepts data loses meaning. The analysis therefore points to the need for both competence in conceptual work and clear responsibility for the management of shared information models, including funding and long-term ownership.

#### Brief assessment


SAMT-BU-017 makes clear that coherent services require shared understanding before shared solutions. The case shows that work on concepts and information models is a strategic investment that lays the foundation for legally correct practice, effective collaboration and sustainable digitalisation.

## SAMT-BU-018 – From UDE in the City of Oslo: Vulnerable children in school and interdisciplinary follow-up


| **ID and title of ****use****-****case** | **SAMT-BU-018 – From UDE in the City of Oslo: Vulnerable children in school and interdisciplinary follow-up** | **Unique local identifier and title for the ****use case****. The title should describe the goal as a short, active verb phrase.** |
| --- | --- | --- |
| Brief description | The use case concerns: From UDE in the City of Oslo: Vulnerable children in school and interdisciplinary follow-up. (Based on the case register.) | Concise description of the use case, including context and scope. Describe what is included and what is outside (the black-box scope). |
| Primary actor | • School leader/head teacher (coordinates measures and follow-up) | The role that initiates the use case and holds the main goal. There shall be only one primary actor. |
| Secondary actors | • Teachers• PPT• Parents and guardians• Collaboration tool (BTI/stafettlogg-like)• IAM/access management | Other roles or systems that support or are affected by the use case. May be users or technical systems. |
| Stakeholders | • Pupil/parent or guardian – rights and understandable collaboration• School/PPT – effective and safe follow-up• Management – overview, allocation, approval• Supervisory authority – compliance (duty of confidentiality/consent) | Names of stakeholders and their primary interest in the goal the use case describes. There may be several stakeholders. |
| Specific considerations (overall) | To be clarified. | Particular implications and considerations beyond general legal and architecture requirements, e.g. relating to AI, privacy, security and universal design. |
| Accessibility | • Plain language• Multiple languages/channels (text/audio/image) where relevant | Identified considerations relating to universal design and accessibility for different user groups. |
| Generative AI | • Decision support/drafts only, with human control• Requirements for transparency/source basis for suggestions | Identified considerations relating to the use of generative AI, e.g. transparency, verifiability, bias and human control. |
| Diagram | USER FLOW  [Parent/guardian] <-> [School] <-> [PPT] : holistic pupil follow-up (coordinated)DATA FLOW  [Collaboration tool] -> [Role-based access] -> [Measures/tasks]  [School/PPT system] <-> (standardised data) <-> [Management data/insight] | Visualisation showing the data flow between actors and system components that enable the use case. Use the recommended symbol set (cf. Appendix C2). |
| Implications for interoperability | Data flows that must be supported: identity/access, core information for the use case, status changes/events, and traceable logging. | Identification of which data flows must be supported, and which interoperability standards should be used where possible. |
| Notes | Further details/link: https://digdir.sharepoint.com/:w:/r/sites/Prosjekt_Medfinsknad2025/Delte%20dokumenter/Case/18%20Case%20fra%20UDE%20i%20Oslo%20kommune.docx?d=w1004c689a84447149253c7e7b7e597aa&csf=1&web=1&e=rjp5VwSource document (step 2): 18 Case fra UDE i Oslo kommune.docx | Supplementary notes and references used or mentioned elsewhere in the table. |


### Rationale (analysis) – SAMT-BU-018


*Holistic basis for governance and decision-making for management across services*

#### UFO – ontological clarification


This use case shifts the focus from operational service delivery to **governance and decision-making**. Ontologically, the case concerns aggregated representations of reality: indicators, status overviews and compilations that are not services in themselves, but abstract from them. The challenge arises when such representations become detached from the underlying events and relationships on which they are based. The analysis shows that management information loses value if the link to actual measures, responsibilities and results is not clear and verifiable.

#### Legal method


From a legal perspective, the use case brings to the fore the relationship between management information and privacy. Even when data is aggregated, combinations of information can provide insight that approaches personal data or sensitive patterns. The analysis points out that management information must be designed so that it provides the necessary insight without opening the way for unlawful re-identification. The case therefore points to the need for a clear framework for what kind of management information is legitimate to produce and use.

#### Toulmin – implicit argumentation


The implicit claim in the use case is that better decisions presuppose a better overview. The grounds for this claim lie in the description of fragmented, sector-by-sector reporting. The reservations concern the fact that management information is never neutral; it also shapes which problems become visible and which remain hidden. The case therefore argues for management information that is balanced and anchored in actual service pathways, not for more reporting in itself.

#### SWOT – strategic assessment


The strength of this use case is that better management information can have a significant effect on prioritisation and use of resources. The weakness lies in the risk of indicators becoming goals in themselves. The opportunity lies in establishing management overviews that provide insight across services, while the threat is that a lack of coherence between data and practice leads to erroneous decisions.

#### iStar – goals and dependencies


The analysis makes visible that management depends on the underlying services delivering consistent and understandable information. At the same time, the services depend on governance requirements being realistic and relevant. The use case points out that when this mutual dependency is not handled explicitly, tensions arise between reporting and actual service work.

#### TOGAF / ArchiMate – architecture implications


The architecture implication of the use case is that management information must be built on clear information models and defined data sources. This points to the need for a clear separation between operational systems and analytical layers, where data can be compiled without disrupting service delivery. Such an architecture strengthens both the quality of the decision-making basis and trust in the figures.

#### KF extended NIF/EIF – interoperability


The use case shows that interoperability at governance level presupposes maturity in all underlying layers. Without shared concepts, a reliable data basis and clear allocation of responsibility, management information will become fragmented and difficult to compare. The analysis therefore points to the need for holistic governance of both competence and finances relating to governance and analysis functions.

#### Brief assessment


SAMT-BU-018 makes clear that coherent services also require coherent governance. The case shows that good decisions presuppose management information that is anchored in actual service practice, verifiable and used with awareness of both opportunities and limitations.

## SAMT-BU-019 – StatPed - applications for assistance from the educational psychology service in the municipality


| **ID and title of ****use****-****case** | **SAMT-BU-019 – ****StatPed**** - applications for assistance from the educational psychology service in the municipality** | **Unique local identifier and title for the ****use case****. The title should describe the goal as a short, active verb phrase.** |
| --- | --- | --- |
| Brief description | The use case concerns: StatPed - applications for assistance from the educational psychology service in the municipality. (Based on the case register.) | Concise description of the use case, including context and scope. Describe what is included and what is outside (the black-box scope). |
| Primary actor | (to be clarified) | The role that initiates the use case and holds the main goal. There shall be only one primary actor. |
| Secondary actors | • (to be clarified) | Other roles or systems that support or are affected by the use case. May be users or technical systems. |
| Stakeholders | • (to be clarified) | Names of stakeholders and their primary interest in the goal the use case describes. There may be several stakeholders. |
| Specific considerations (overall) | To be clarified. | Particular implications and considerations beyond general legal and architecture requirements, e.g. relating to AI, privacy, security and universal design. |
| Accessibility | • (to be clarified)• (to be clarified) | Identified considerations relating to universal design and accessibility for different user groups. |
| Generative AI | • (to be clarified)• (to be clarified) | Identified considerations relating to the use of generative AI, e.g. transparency, verifiability, bias and human control. |
| Diagram | USER FLOW (conceptual)  [End user] --> [Service/Front end] --> [Caseworker/Adviser] --> [Decision/Follow-up]DATA FLOW (conceptual)  [Client/portal] -> [Specialist system A] -> (API/Event) -> [Specialist system B] -> [Reporting/Log] | Visualisation showing the data flow between actors and system components that enable the use case. Use the recommended symbol set (cf. Appendix C2). |
| Implications for interoperability | To be clarified. | Identification of which data flows must be supported, and which interoperability standards should be used where possible. |
| Notes | (no notes in the case register) | Supplementary notes and references used or mentioned elsewhere in the table. |


### Rationale (analysis) – SAMT-BU-019


*Learning, improvement and reuse of experience across services*

#### UFO – ontological clarification


This use case directs attention to **experience as a social and organisational resource**, not just as individual events. Ontologically, the case concerns how experiences arise through action, assessment and outcome, and how these can be abstracted and reused without losing context. The challenge is that experience often remains tacit or locally anchored, so that the organisation as a whole does not learn systematically from what happens in individual cases.

#### Legal method


From a legal perspective, the use case brings to the fore the boundary between learning and privacy. When experiences are to be reused, they must be detached from identifiable information and specific individual cases. The analysis points out that a lack of structure for anonymisation and aggregation often means that learning either does not take place, or happens informally and in a way that is difficult to verify. The case therefore points to the need for a clear framework that enables learning without undermining rights and the duty of confidentiality.

#### Toulmin – implicit argumentation


The implicit claim in the use case is that the quality of services improves when experiences are shared and used systematically. The grounds for this claim lie in the description of recurring challenges and known patterns that are not translated into improvement. The reservations concern the fact that experiences are always contextual and cannot be generalised uncritically. The case therefore argues for structured reflection and reuse, not for simple «best practice» lists.

#### SWOT – strategic assessment


The strength of this use case is that the potential for improvement is large and long-lasting. The weakness lies in learning often being deprioritised in a busy everyday working life. The opportunity lies in establishing shared arenas and mechanisms for sharing experience, while the threat is that a lack of system leads to the same mistakes being repeated over time.

#### iStar – goals and dependencies


The analysis makes visible that both management and employees depend on experiences actually being collected and shared in a meaningful way. At the same time, the services depend on learning leading to real change, not just documentation. The use case points out that when this dependency is not supported by structures and incentives, learning remains random and dependent on individuals.

#### TOGAF / ArchiMate – architecture implications


The architecture implication of the use case is that learning and improvement must be supported by mechanisms that can collect, analyse and communicate experiences across services. This points to the need for analytical and knowledge-support components that are connected to, but do not disrupt, operational service delivery. Such an architecture makes continuous improvement possible in practice.

#### KF extended NIF/EIF – interoperability


The use case shows that interoperability is also about the ability to learn together. Technology can support the collection and sharing of experiences, but without a shared culture, competence and prioritisation, the effect will be limited. The analysis therefore points to the need for both competence development and financial room for systematic improvement work across services.

#### Brief assessment


SAMT-BU-019 makes clear that coherent services are created not only through good structures, but also through continuous learning. The case shows that the ability to translate experience into improvement is crucial for quality, sustainability and development over time.
