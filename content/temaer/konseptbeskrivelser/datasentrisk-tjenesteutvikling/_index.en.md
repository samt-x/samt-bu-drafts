---
id: 39286298-056f-4d68-9fe0-cdea507f59cb
# id: auto-generated – copied values are overwritten automatically on push
title: "Data-centric service development"
linkTitle: "Data-centric service development"
weight: 10
lastmod: 2026-05-30T23:18:51+02:00
last_editor: Erik Hagen

---

*Concept description for SAMT-BU – draft for the architecture group*

---

## 1. Summary

Data-centric service development is an architectural commitment to data – with shared, explicit meaning – being what is stable, while applications are replaceable projections onto the data. This concept description commits SAMT-BU to that direction, and to realising it through a virtual, layered knowledge graph with data product orientation.

The background is easy to state and hard to solve: coherent services for children and young people across kindergarten, school, municipality and state require that those involved understand the same concepts in the same way – that "pupil", "decision", "consent" and "place of residence" mean what they should, also when data is retrieved from different agencies. Today's application-centric landscape places this understanding in code, spread across each line-of-business system, where it must be maintained anew for each integration. Data-centric architecture moves the meaning out of the code and into a shared semantic layer that the applications – and in time the AI agents – build against.

The concept rests on three pillars: *data-centric* as an architectural choice (data, not applications, is what is stable), *data product orientation* as organisation (data is delivered as products with clear stewardship responsibility, contracts and semantic annotation), and a *virtual knowledge graph* as realisation (data remains with its authoritative sources, and a layered ontology binds them together through mapping). The decisive property is that the graph grows monotonically: new concepts can be added without breaking what already works. It is this property that allows value to be realised gradually, pilot by pilot, without waiting for a finished model.

The concept is anchored in international frameworks – in particular the EU's operational interoperability mechanisms ([MIMs Plus](#mims-plus)) and [SEMIC's Core Vocabularies](#semic-core-vocabularies) – so that the Norwegian public sector can connect to the European ecosystem of shared concepts rather than build a special variant.

Equally important is what the concept does *not* do. It does not centralise data, it does not replace existing line-of-business systems, and it does not choose technology, products or suppliers – such choices belong to the target architecture and the architecture group's further work. The concept description commits the direction, not the decisions beneath it.

The document can be read linearly or as a reference: the concept choice with the alternatives considered (section 3), the architectural realisation (section 4), the relationship with the application's own language (section 5), the international anchoring (section 6), the implications for pilots, partners and AI (section 7), and finally the scope and the open questions that belong to the further work (section 8).

---

## 2. Introduction

This document is a concept description for **data-centric service development** in SAMT-BU. It is a draft, placed under [Concept descriptions](../), and is intended as input to the project's architecture group. It is not a definitive answer, and it does not replace the target architecture or the further architecture discussion the project is to carry out. It is a working document that commits the direction, so that the next steps can be taken on a reasoned basis.

### Background

The application on which SAMT-BU is based uses expressions such as "middle layer", "common information models", "service catalogue" and "data virtualisation" as placeholders for something for which there was no established Norwegian term when the application was written. These terms point in a particular architectural direction, but they are not self-describing in the sense that they tell how the direction is to be realised. That is the job this concept description takes on.

Now that an architecture group has been established and the project is in its operational phase, it is also time to introduce the precise language the concept requires – data-centric paradigm, data product orientation, virtual knowledge graph, layered ontology. These terms are not new to the international professional community, but they are not yet established in Norwegian public-sector vocabulary. Part of this concept description's job is to make the connection between the project's existing language and the precise professional language explicit.

### What this document is

The document is:

- An **architectural commitment** to the data-centric paradigm realised through data product orientation and a gradually extensible virtual knowledge graph
- An **anchoring in international frameworks** – in particular MIMs Plus, SEMIC's Core Vocabularies, and data product orientation with a semantic anchor
- A **bridge** between the application's language and the precise professional language the concept requires
- A **draft and input** that the architecture group can discuss, refine or reject

### What this document is not

It is equally important to be explicit about what the document is not, so that it is read correctly:

- *Not a target architecture.* Concrete technology choices, supplier choices, infrastructure set-up and product choices belong to the target architecture and come later.
- *Not a centralised data solution.* A virtual knowledge graph means that data remains with its authoritative sources; the integration takes place in the semantic layer above.
- *Not "wait for the big graph before we deliver".* The architectural direction is gradually extensible – the pilots deliver value along the way, not at one big completion.
- *Not that existing line-of-business systems are to be replaced.* The concept describes how existing systems can be connected to the semantic infrastructure, not that they are to be replaced.
- *Not a critique of individual solutions.* We mention FINT, the National Data Catalogue (Felles datakatalog) and the Bergen study by name because they are concrete reference points, but the purpose is positioning, not disparagement.
- *Not an academic exercise.* Every part of the concept has been chosen to work operationally at public-sector scale, not to meet a theoretical ideal.
- *Not a description of the current situation.* A thorough mapping of existing line-of-business systems, data management and collaboration patterns in the affected sectors is part of the architecture group's own work and does not belong here.

### How the document is structured

The document can be read linearly, but it is also structured so that readers can go directly to the part that is most relevant:

- **Concept choice** for those who want to know which alternatives have been considered and why we land where we do
- **The realisation** for the technical core: virtual knowledge graph, layered ontology, data products, applications
- **Relationship with the concept outlined in the application** for the connection between the application's language and the concept we present
- **International anchoring** for the connection to the EU's operational interoperability framework (MIMs Plus, Core Vocabularies)
- **Implications** for what the concept means for pilots, partners and AI strategy
- **Scope and open questions** for what belongs to the architecture group's further work

The concept description is written with the ambition of being readable for managers and professionals without a semantic web background in the first paragraphs of each section, and precise enough for architects further down. Each section typically ends with a pointer to what is left to the architecture group or the target architecture.

---

## 3. Concept choice

The concept choice should not be made before it has been justified. In this section we show which alternative concepts we have considered, which requirements we have measured them against, and why we land where we land. The intention is that the reader should be able to disagree with the conclusion on a reasoned basis, not reject it because the alternatives were never mentioned.

### The requirements the ambition sets

The ambition of coherent, cross-sector services – across everything the public sector is responsible for – sets these requirements:

**1. Data is accessed where it is owned.** The application is explicit that we shall not copy or move data out of context. The National Population Register (Folkeregisteret), the Central Coordinating Register for Legal Entities (Enhetsregisteret), the cadastre (Matrikkelen) and the line-of-business systems in the municipalities stay where they are.

**2. Semantic interoperability across.** It must be possible to know whether "cohabitant" at NAV, the Tax Administration and the population register refers to the same entity, and where they differ. This applies to hundreds of similar concepts.

**3. Gradual extension without breakage.** It must be possible to add new concepts without invalidating existing data or services. Backward compatibility shall be a fundamental property of the architecture, not an operational exercise every time something changes.

**4. International interaction.** The EU's operational frameworks – Single Digital Gateway, Once-Only Technical System, Data Spaces and MIMs Plus – are built on shared semantic data models (SEMIC's Core Vocabularies, CPSV-AP, CCCEV, DCAT-AP and related standards). These models are RDF-based, even where the exchange format on the wire is XML or JSON. Norway must be able to connect to this ecosystem of shared concepts, not build a special variant. *Detailed mapping against MIMs Plus follows in section 6.*

**5. AI accountability.** If the public sector is to use AI agents in service delivery, the answers must be verifiable and anchored in authoritative sources with explicit meaning.

**6. Shared concepts for coherent user journeys.** User journeys across agencies require that the same concept is understood consistently. This is the whole rationale behind the project.

### Alternatives considered

We have considered seven concepts, from the most traditional to the most ambitious:

**A. Centralised data store (data warehouse, data lake).** Classic BI approach where data is copied to one central storage location. Works well for analysis, but directly breaks the requirement that data is accessed where it is owned. At cross-sector scale, copying, update cycles and governance become unmanageable, and personal data raises significant legal questions.

**B. Master Data Management (MDM) alone.** Strong for a limited set of core concepts (person, business, address). But MDM is not in itself an architectural paradigm – it does not address the broader question of how services and applications should relate to each other. We will use principles from MDM on selected base data, but cannot build the whole concept on it.

**C. ESB with canonical data model (hub-and-spoke / FINT style).** Well-proven approach where a central integration bus and a shared data model bring systems together. Novari's FINT is a modern realisation for the county authorities and part of the project's source of inspiration. But experience shows two recurring problems: the canonical model becomes a bottleneck that is difficult to evolve, and changes often break backward compatibility with connected systems. This does not scale to all public services over decades.

**D. API mesh or "data fabric" without a semantic layer.** Modern API-oriented integration (REST, GraphQL, events) solves technical connections, but the semantics still lies implicitly in the code of each consumer. Each new integration requires a new interpretation of what the concepts mean. The N² problem is moved, not removed.

**E. Data mesh without a knowledge graph.** Data products with ownership, contracts and federated governance solve a lot organisationally. But data mesh in its original form does not address the semantic fragmentation between domains. Consumers still have to normalise the semantics themselves at each connection.

**F. Data-centric on relational models.** [McComb](#mccomb-2019) argues in [*The Data-Centric Revolution*](#mccomb-2019) (ch. 8–9) that data-centric architecture is in principle also possible with traditional relational models. That is technically correct. But the complexity grows exponentially with the number of organisations, concepts and pace of change. The monotonic extension property that linked data provides is difficult to achieve when schemas are strict. At Norwegian public-sector scale, this variant becomes theoretically feasible but practically delaying.

**G. Data-centric with a virtual knowledge graph.** The data-centric paradigm realised through a virtual, layered ontology that references the data where it is owned. Data products expose data with semantic links to the ontology. This is the concept we recommend.

### Comparison

| Concept | Data where owned | Semantic interop. | Gradual extension | EU compatibility | AI accountability | User journeys |
|---|:---:|:---:|:---:|:---:|:---:|:---:|
| A. Data warehouse / data lake | ✗ | △ | ✗ | ✗ | △ | ✗ |
| B. MDM alone | △ | △ | ✗ | ✗ | △ | △ |
| C. ESB / canonical model (FINT style) | ✓ | △ | ✗ | ✗ | ✗ | △ |
| D. API mesh without semantics | ✓ | ✗ | △ | ✗ | ✗ | ✗ |
| E. Data mesh without knowledge graph | ✓ | ✗ | △ | △ | ✗ | △ |
| F. Data-centric on relational models | ✓ | △ | △ | △ | △ | △ |
| **G. Data-centric + virtual knowledge graph** | **✓** | **✓** | **✓** | **✓** | **✓** | **✓** |

Legend: ✓ meets, △ partially, ✗ does not meet. The assessments are qualitative and open to discussion. The table's value lies in showing the *pattern*, not in being precise in every single cell.

### Convergence, not maximisation

The argument for alternative G is not that it is "best" on every single dimension. The argument is that it is the only concept that **simultaneously** meets all the requirements, given the level of ambition. Alternatives A–F are each good on some criteria, and some are good on several – but none handles the combination.

This should not be read as saying that relational models are bad, that APIs are superfluous, or that MDM is wrong. On the contrary, several of these elements will be part of the actual realisation: data typically remains stored in relational databases at the owners, integrations often take place via APIs, and MDM principles are applied to selected base data. Concept choice G is about the *semantic layer above* this, and about how data products expose meaning – not about replacing underlying technology.

### What the concept choice does *not* do

It is important to be explicit about what this choice implies and does not. We have chosen a **paradigm** (data-centric service development) and an **architectural pattern** (virtual knowledge graph with federated layered ontology and data product ownership). We have **not** chosen:

- Concrete technologies (e.g. [RDF](#rdf-and-sparql) vs. property graph, [SPARQL](#rdf-and-sparql) vs. Cypher, choice of triplestore)
- Concrete tools for ontology modelling and governance
- Concrete infrastructure (cloud vs. on-prem, which shared solutions are extended)
- Concrete suppliers

Such choices belong in the target architecture, with the architecture group, and in the pilots. The concept description commits the direction, not the decisions beneath it.

---

## 4. The realisation: virtual knowledge graph with layered ontology

This section describes how data-centric service development is to be realised architecturally. We go through the virtual knowledge graph as a pattern, the layered ontology that structures the semantic content, the data products that carry the data, and how these building blocks fit together in an information architecture that can grow gradually.

The section is the most technical in this concept description. It is nevertheless written to be understandable for the architecture group and professional leads who are not semantic web specialists. We leave concrete technology choices to the target architecture.

### 4.1 The virtual knowledge graph as architecture

A **knowledge graph** is a graph where nodes represent concepts and entities, and edges represent the relationships between them. When the knowledge graph is built on an explicit **ontology** – a formal model of the concepts and how they relate – the relationships become machine-readably typed. The concepts have a defined meaning that both humans and programs can reason over.

[Gioia](#gioia-2024) describes three architectural variants of knowledge graph ([*Managing Data as a Product*](#gioia-2024), ch. 11):

1. **Data-centric (materialised) knowledge graph.** Data lives inside the graph. Applications write and read directly against the graph. McComb's ideal state.
2. **Knowledge warehouse (materialised).** Data is copied from the source systems into the graph for read access. Ownership remains with the sources.
3. **Logical knowledge warehouse / virtual knowledge graph.** Data remains in the source systems. The graph refers to them through mapping concepts.

For SAMT-BU, choosing the virtual variant is not a pragmatic concession; it is the right choice. The Norwegian public sector has authoritative registers – the National Population Register, the Central Coordinating Register for Legal Entities, the cadastre, Sikt's registers – which neither can nor should be moved into one central graph. Semantic integration is achieved through mapping between the data products and a shared ontology, not through data centralisation.

Concretely, this means that:

- Data remains stored with its authoritative sources, in their existing formats and systems. (What an authoritative source is, and what "ownership" means in this context, is clarified in 4.3.)
- A shared ontology defines which concepts the systems talk about.
- A separate *mapping layer* – between the data sources and the ontology – links elements in the data to the concepts in the ontology. This layer is a separate artefact, not part of the ontology itself.
- Consumers can pose questions against the ontology as if the data were there as triples, either actually stored or virtually computed; the questions are translated into operations against the source systems.

Gioia himself recommends this architecture as a realistic starting point for modern organisations, and points out that the fully data-centric variant (alternative 1) may be a potential *long-term goal* once the ontology infrastructure is mature. For SAMT-BU's time frame, it is the virtual variant that is feasible and that the downstream value is to be drawn from.

### 4.2 The layered ontology

One ontology for the entire public sector is neither practical nor desirable. Different sectors model reality differently because they have different purposes – a teacher thinks about "pupil" differently from an accountant or a social worker – and it is right that the models reflect this. At the same time, they must fit together where there is a need for interaction.

The layered approach organises this into four layers:

**Upper ontology.**
Universal concepts that transcend domains: object, event, time, place, agent, role. Established standards exist ([BFO](#bfo) – Basic Formal Ontology, [GIST](#gist)). A Norwegian public concept should be expressible as a specialisation of these abstract building blocks.

**Domain ontology.**
Concepts that are common to "public administration in Norway": person (with address, identifier, citizenship), business, service, decision, event, consent, power of attorney, ruling. This is the core model, and this is where most of the semantic work takes place for the project's ambition of coherent services. SEMIC's Core Vocabularies (Core Person, Core Public Service, Core Organization, Core Location, CCCEV) provide an EU-linked starter pack for this layer – not as requirements we submit to, but as natural anchor points that save work and guarantee cross-border compatibility.

**Subdomain ontologies.**
Sector-specific extensions: education (pupil, teacher, subject, assessment, diploma, admission), health, social, justice, labour. Each sector models its domain and extends the domain ontology where specialisation is needed. SAMT-BU naturally starts in the education domain.

**Application ontologies.**
Models linked to a specific service or pilot, for example "change of school when moving between municipalities" or "sharing a diploma with an employer". This is where concrete user journeys are modelled, and where most of the project's pilots will live.

The layers are in an **extension relationship**: a subdomain concept extends a domain concept, which extends an upper concept. This means that an application working with education-specific concepts automatically inherits the general properties from the domain and upper layers without having to repeat them.

#### Why the layering solves the "cohabitant" problem

An example that illustrates the value: the concept *cohabitant*. The domain ontology can define a core concept "Cohabitant" with a minimum definition – two persons who share a household without being married. The Tax Administration's subdomain can extend this with tax criteria (continuous period of living together, shared assets); NAV's subdomain with social security law criteria; the population register's with address-based criteria.

The concepts are different – rightly so, for they serve different purposes – but they are **explicitly linked** to the same core concept through the ontology. Systems that retrieve data from all three can then know both where they are alike and where they differ. It is this kind of precision that today's fragmented model landscape does not provide.

#### Federated modelling teams

The layers have different owners. The domain ontology must be owned centrally – the whole point is that it is shared. The subdomain ontologies are owned by the respective sectors; the application ontologies by service owners or pilots.

Gioia calls the central modelling organisation a **federated modelling team**: representatives from each sector involved, with a mandate to negotiate and manage the shared concepts. For SAMT-BU, this will be a joint body with delegates from [Digdir](#digdir), KS Digital, Udir, Sikt, HK-dir, STAF and SSB. The composition and governance do not belong to the concept description; but it is this kind of mechanism that must be established for the concept to work in practice.

### 4.3 Authoritative sources, data products and applications

The word "ownership" is used about data so broadly in the Norwegian public sector that it covers three different relationships which must be kept separate architecturally. The concept description requires that we make this distinction clear, because bundling the three into one concept is part of the problem we want to solve.

#### 4.3.1 Three meanings of "ownership"

**The data subject's ownership.**
Personal data belongs to the person the data is about. Business data belongs to the business. This is a fundamental right. The operational realisation in the target architecture is **digital wallets** – the EUDI Wallet for persons, and corresponding constructs for businesses. It is the data subject who controls which data is shared, with whom, and under what conditions.

**Stewardship responsibility (legal basis or consent).**
A public body may have the *right to process* certain data – either through a legal basis or through consent from the subject. This is a legal-administrative relationship, not a property right. The Tax Administration does not "own" the taxpayers or their income information; the agency has a legal basis for specific processing for specific purposes. When a municipality processes data about pupils, it has a legal basis or consent – it is not an "owner" in any meaningful sense.

**Data product responsibility.**
When this concept description refers to a "data product owner", we mean something more specific: the party with *operational responsibility* for managing a data product – quality, availability, semantic annotation, contracts and life cycle. This is a stewardship and delivery responsibility, not a property right. The National Population Register has data product responsibility for authoritative personal identification on behalf of society; it does not "own" the persons.

The three relationships can occur simultaneously on the same data, but they are different relationships and must be able to be discussed separately. Much of the confusion in today's debate about data sharing, consent and data minimisation comes from mixing them up.

#### 4.3.2 Today's fragmented situation

Through an application-centric development history, the Norwegian public sector has ended up with a large number of line-of-business systems that each act as the *de facto* owner of "their" data – with their own data models, their own identifiers and their own interpretations of shared concepts. This is not an innocent fragmentation. It is what McComb diagnoses as the application-centric quagmire ([*Software Wasteland*](#mccomb-2018), ch. 3): each application creates its own reality of data, integrations between them multiply (N²), and shared concepts melt into local variants that cannot be reconciled.

The approach of "gathering metadata in a shared data catalogue and consolidating over time" has proved difficult to realise in practice, because the consolidation work competes with ongoing priorities at each data owner. The result is that the catalogue grows with descriptions of overlapping and inconsistent datasets without the fragmentation itself being reduced.

The concept description does not accept this state as a starting point. Data-centric architecture presupposes a clean-up job in which clear authoritative sources are established, and in which applications – new or old, traditional or AI-based – are consumers, not owners.

#### 4.3.3 Authoritative sources and data product responsibility

The concept distinguishes between two fundamental roles in the data landscape: **authoritative sources** and **applications**.

Authoritative sources have the authority of truth for a set of concepts and offer them to the rest of the ecosystem. Examples we already have today:

- *The National Population Register* for personal identification, name and residential address
- *The Central Coordinating Register for Legal Entities* for businesses
- *The cadastre (Matrikkelen)* for property and buildings
- *Sikt's education register* for educational offerings and institutions
- *Sikt's register of proof of competence* for diplomas and results from education

These shall remain authoritative. New authority for other concepts shall be established in the same way: clear data product responsibility, documented contracts, semantic annotation. A central part of the project's work is to clarify where clear authoritative sources are lacking – for example for municipal services for children and young people – and to clean up where there are currently several overlapping authorities for the same concept.

The authoritative sources offer themselves as **data products** with the properties Gioia describes: clear data product responsibility (in the third sense of "ownership"), explicit contracts, self-describing metadata, and semantic annotation that binds the fields to the ontology. The last of these – semantic annotation, for example through the Data Product Descriptor Specification (DPDS) with "s-context" annotations – is what links the individual data product to the layered ontology described in 4.2. A field such as *date of birth* in the National Population Register's personal data can be annotated as an instance of *birthDate* in the Core Person Vocabulary, which in turn is a specialisation of a time expression in the upper ontology.

The technical mapping mechanism between relational databases or other data sources and the semantic representation can be formalised using established standards: **[R2RML](#r2rml-and-rml)** for relational data, **[RML](#r2rml-and-rml)** for semi-structured data (JSON, XML, CSV). These are practical tools the architecture group can build on, not corporate strategic choices.

It is important to emphasise: the authoritative sources continue to use their existing technologies – relational databases, REST APIs, event queues. It is the **semantic overlay** (annotations, mapping) that is new, not the data store itself.

#### 4.3.4 Applications as consumers – including AI agents

Everything that is not an authoritative source is an **application** in the concept's sense: case management systems, citizen-facing interfaces, line-of-business systems, analysis and statistics tools, dashboards, and **AI agents**.

The same principle applies to all of these: they are consumers, not owners. Concretely:

- They shall *not* invent their own data models for concepts that exist in the shared ontologies.
- They shall *not* create parallel stores of data that is authoritative elsewhere.
- They shall *not* retrieve data, transform it into their own representation, and become a de facto authority for "their" version. This is precisely how today's quagmire arose.
- They shall respect the data subject's consents and powers of attorney as expressed in wallets or equivalent mechanisms – not keep their own copies of consent registers where this can be avoided.

For **AI agents** this is particularly important because there is considerable market hype around agents "learning" and "remembering" – which can easily slide into agents de facto owning or creating data. Data-centric architecture is probably the only way to integrate AI agents into the Norwegian public sector without creating a new generation of locked-in, non-interoperable systems that repeat the mistakes of the first generation of line-of-business systems. An agent that answers a citizen about their child's school offering shall retrieve facts from authoritative sources via the knowledge graph, not from a local knowledge store it has constructed itself. The semantic knowledge graph is the stable foundation; the agents – like the applications before them – are replaceable projections.

A consequence McComb makes explicit: in a data-centric architecture you do not need more applications over time – you need fewer, because much of what today's applications do is keep track of their own local data models. When that job is done by the semantic foundation, applications become simpler and more replaceable.

### 4.4 How the information architecture fits together

The data-centric architecture can be organised into four layers (Gioia, ch. 11), as shown in the table. The "responsibility" column must be read here in line with the distinction in 4.3 – it is stewardship and delivery responsibility, not a property right.

| Layer | What it is | Responsibility |
|---|---|---|
| Data plane | The data itself in the source systems | Authoritative sources / data product owners |
| Information plane | Data + metadata (structure, quality, availability, terms of use) | Authoritative sources / data product owners |
| Knowledge plane | Shared ontology and semantic links | Federated modelling team |
| Intelligence plane | Services, decisions, applications (incl. AI agents), end users | Service owners and users |

Authoritative sources and data product owners take care of the data plane and the information plane – they deliver data with descriptions of what is there. The knowledge plane – the ontology – is managed in a federated way by the modelling team. The intelligence plane is where the value is realised: coherent services, case management, statistics, and AI-assisted helpers that all draw their knowledge from the underlying layers.

#### A worked example: change of school when moving

We take an example from the project's current pilots to show how it fits together. A 14-year-old child moves to a new municipality in the middle of the school year.

- **In the data plane**: The National Population Register updates the address. The former municipality's line-of-business system has the pupil registered with assessments and subject choices. The new municipality has schools with available places registered in its line-of-business system.
- **In the information plane**: Each of these is described as data products with metadata about what is offered, who owns it, and how access works.
- **In the knowledge plane**: The domain ontology has concepts for *person*, *place of residence*, *event*, *decision*. The subdomain ontology for education links them with concepts such as *pupil*, *school*, *class*, *change of school*, and establishes the relationship between "moving" as an event and "change of school" as a triggered service need.
- **In the intelligence plane**: A service – perhaps with an AI-assisted interface for parents – sees that the event "moving" for a person below school-leaving age triggers the need "change of school". The service finds relevant data products via the knowledge graph, applies business rules on school catchment area, capacity and continuity, and proposes actions for the municipality and the parents.

Essential: no one has built a specific "Population Register-X-Education System-Y-Municipal System-Z" integration. The value lies in the user journey being assembled *on top of* a stable semantic infrastructure. New user journeys – transition from primary/lower secondary to upper secondary, follow-up of dropout, sharing a diploma with an employer – do not require new integrations; they require new questions to the knowledge graph, and often only small extensions of the application ontology.

### 4.5 Gradual build-out – an evolutionary architecture

The layered ontology and the virtual knowledge graph are developed **not as one big modelling effort before anything is delivered**. This is a central part of the concept choice, and it is what makes the architecture practically feasible at public-sector scale.

Linked data and RDF have a decisive property: **monotonic growth**. A new concept, a new relationship, a new mapping can be added without invalidating what is already there. Existing systems, existing data, existing queries continue to work. This is in contrast to canonical data models, where model changes typically break backward compatibility, as we discussed under alternative C in the concept choice (section 3).

In practice, this means that:

- **The pilots drive the modelling.** A new pilot starts by identifying which concepts are missing in the ontology, and adds them. No pilot waits for a "finished ontology". This is Gioia's principle that ontologies are modelled only when a concrete use requires it, applied to the public sector.
- **Each pilot contributes to the next.** The concepts modelled for the change-of-school pilot are available to later pilots involving transitions between levels of education, transition to working life, or entirely different services that benefit from the same conceptual apparatus. The investments accumulate.
- **Existing shared solutions are extended gradually.** The National Data Catalogue on data.norge.no is given extensions for new concept and model catalogues. Sikt's education register is given semantic annotations that link it to the knowledge graph. None of these has to be changed all at once.
- **Federated modelling reduces bottlenecks.** When several modelling teams work in parallel on different subdomains, and only the central domain ontology requires broad consensus, it is practically possible to scale the modelling work.

It is this combination – a semantic foundation with monotonic growth, data products with existing ownership, and pilot-driven modelling – that makes the virtual knowledge graph a realisable architecture for the Norwegian public sector, not just an academic model.

How this relates to the project's existing framework – and in particular to the "middle layer" and "common information models" that the application uses – is dealt with in section 5.

### 4.6 Data-centric access control

Access control follows the same logic as the rest of the architecture: what is stable is the data, not the services that expose it. An application-centric landscape asks "is user X allowed to call service Y?". A data-centric architecture asks "is user X allowed to see this data, regardless of which service exposes it?". The distinction is not academic in SAMT-BU's domain, where sensitive information about children and young people flows across kindergarten, school, municipality and state: it is the data and its content that is regulated, while the APIs are replaceable projections. Access rules tied to the service must be rebuilt for each new service and fit poorly with the logic of the virtual knowledge graph.

The consequence for the concept is one principle: rights are attached to data, not to APIs. It is meaningful to express a right against an abstract, persistently identified resource – a dataset – regardless of whether it is exposed via REST, a SPARQL endpoint or file download. A rule can then say that "caseworkers in the child welfare service may use information from [dataset] for purpose [Y] in period [X]", and remain valid when the technical distribution is replaced. This ties in with the three meanings of "ownership" in 4.3.1: access control enforces the legal and stewardship control over the data, not a technical endpoint. [ODRL](#odrl) is the standard built to express such rights against datasets.

How this is enforced by machine – the relationship between policy expression and enforcement architecture, and what today's national infrastructure supports – is a target architecture and architecture question, not a concept choice. It is treated as an open question in 8.2.

---

## 5. Relationship with the concept outlined in the application

The application outlines a concept that is solid enough as a starting point for the project. Further developing and operationalising the concept is a central part of what the project itself is to do, and this concept description is the first step in that further development. The formal concept phase is covered by Bergen Municipality's study *Konseptforslag – felles kommunal dataforvaltning* (Concept proposal – shared municipal data management, referenced as an annex in the application), which establishes the need for a coordinated approach to data sharing and data management.

SAMT-BU builds on this basic idea, but cannot be limited to the municipal sector. The aim of coherent services for users implies that we must think interoperability in data sharing across sectors. This does not rule out separate solutions in the municipal sector, but it rules out solutions that stand in the way of cross-sector interaction.

In this chapter we show how the terms in the application map to those we have introduced here, and where we go beyond what the application says explicitly.

### 5.1 What the application actually says

The application stated that "new solutions and services are developed against a fixed 'middle layer', decoupled from where or how data is stored. At the same time, data is accessed where it is stored, without the need for local copies." The concept choice study on which the application was based is described as "a concept with common information models in combination with a common service catalogue, as well as common concept and metadata catalogues and associated governance models for collaboration". Novari's **FINT** (Felles INTegrasjoner – Common Integrations) is mentioned as technical inspiration.

The application also uses the expression **"data virtualisation"** explicitly – both as an archive requirement (the Digitalisation Circular table) and as a prerequisite for environmental benefit (K7: data is accessed where it is owned rather than copied).

In summary, this concerns the following elements:

1. A *"middle layer"* through which data is accessed
2. *Common information models*
3. *Common service catalogue*
4. *Common concept and metadata catalogues*
5. *Data virtualisation* as the way data is accessed

The FINT reference sits as inspiration alongside this – assessed as alternative C in the concept choice (section 3).

### 5.2 Mapping of the terms

The application's language is pragmatic and open. The concept description gives these terms a precise architectural content:

**"The middle layer" → the virtual knowledge graph.**
The middle layer in the application was a well-chosen placeholder for something for which there was no established term. What we now make it concrete as is a *virtual knowledge graph* in which the data from authoritative sources becomes available through semantic links to a shared ontology. The property "data is accessed where it is owned, without local copies" is preserved – and reinforced, because it is now unambiguous what kind of structure consumers see when they access data through the middle layer.

**"Common information models" → the layered ontology.**
In the application's language, "common information models" is a collective term for shared representations of concepts. In the concept here, it is realised as a layered ontology (upper, domain, subdomain, application) that allows both common features and sector-specific extensions to be explicit. SEMIC's Core Vocabularies provide EU-compatible starter packs for the domain layer. The layered structure is the architectural property that allows the models to be extended monotonically without breaking existing use – something a flat information model does not provide.

**"Common service catalogue" → service ontology and data product contracts.**
In the application, the service catalogue is conceived as an overview of public services. In the concept, services get their semantic representation in the ontology (at the domain and application layers, naturally based on CPSV-AP), while the operational contracts linked to each service and each data product get their own formalisation ([DPDS](#dpds), ODRL for terms of use). The catalogue thus becomes a composition of semantic descriptions and contract descriptions, not a flat list.

**"Common concept and metadata catalogues" → management structure in and around the knowledge graph.**
The concept catalogue is in practice a human interface to the domain ontology. Metadata catalogues such as [DCAT-AP-NO](#dcat-ap-no) describe data products at a level consumers need in order to find their way. In the concept, these are linked to the knowledge graph and are not separate solutions – which also solves the problem described in 4.3.2 that a catalogue without a structural consolidation mechanism has proved difficult to keep consistent.

**"Data virtualisation" → the virtual knowledge graph.**
This is a direct translation: the application's data virtualisation is precisely the *virtual* variant in Gioia's three-architectures typology (4.1). The semantic richness the knowledge graph adds is a clarification of what virtualisation must entail if it is to be meaningful across sectors – not just access to data without copying, but access with shared meaning.

### 5.3 Where we go beyond the application

Three points where we clarify or extend the language substantially:

**The ownership distinction** (4.3). The application is silent on what is meant when it says "data is accessed where it is owned" – it uses the expression without specifying what kind of ownership. Our three-way division – the data subject's ownership, stewardship responsibility, and data product responsibility – places the project's shared solutions in a clearer picture of responsibilities, and links the EUDI Wallet and digital wallets explicitly to the concept in a way the application did not.

**Applications as consumers, including AI agents** (4.3.4). The application does not mention AI agents directly. Our clarification – that applications shall not be de facto owners of data, and that AI agents are a type of application that gets no exemption – adds an architectural boundary that is critical for responsible AI use in the public sector and that will be difficult to correct afterwards if we wait.

**International anchoring** (6). The application refers to EU Data Spaces, SDGR, Skills Data Space and the EUDI Wallet, but does not make the connection to MIMs Plus and SEMIC's Core Vocabularies explicit. Our clarification that the concept choice coincides with the EU's operational interoperability framework strengthens both the political and the technical justification.

These three points further develop the application's language in areas where the architecture group needs more precision to be able to work operationally with the concept.

### 5.4 The continuity

All central ambitions from the application are carried forward, but made concrete and reinforced:

- *Data is accessed where it is owned, without local copies* – preserved in the virtual knowledge graph architecture.
- *Reduced number of integrations* – strengthened: integrations are made against the ontology and the data product contracts, not against each individual line-of-business system.
- *End users are shielded from a patchy technical landscape* – strengthened through user journeys being composed semantically, not by building new integrations per journey.
- *Reduced development costs through less maintenance in end-user systems* – preserved: monotonic extension of the ontology means that changes in one place do not automatically propagate as integration work elsewhere.
- *Use of national common components* – strengthened: the concept builds explicitly on data.norge.no (DCAT-AP-NO), the National Data Catalogue, and ongoing work at Sikt, Digdir and KS.

The application was in this sense on the right track. The concept description tells where the track leads.

---

## 6. International anchoring

Norway does not build public digital infrastructure in isolation. This section shows how our concept choice – data-centric service development with data product orientation and a virtual knowledge graph – relates to the international frameworks we are to interact with, and which concrete standards are relevant for the target architecture.

### 6.1 Why the EU perspective is guiding

Two of the project's goals make the EU connection non-optional:

- *Cross-border services in education.* Students and pupils cross national borders. Diplomas, proof of competence and admission must be understandable across borders. Skills Data Space, which the application explicitly points to, is already an EU initiative.
- *Single Digital Gateway obligations.* The SDG Regulation also applies through the EEA Agreement. Norway is obliged to make the procedures in Annex II available as fully digital, cross-border services.

It is technically and politically unwise to build a Norwegian special variant and then map out to the EU. It is simpler, and strategically wiser, to build on the semantic foundation the EU ecosystem has already established. This does not mean that we import everything – it means that we take our starting point there instead of inventing in parallel.

### 6.2 EU Data Spaces and DSSC Blueprint

**EU Data Spaces as a framework concept.** EU data policy since 2020 has been organised around the concept of *data spaces* – federated, sector-specific data-sharing infrastructures where data remains with the owner and is shared through standardised contracts and protocols. The EU currently funds data spaces across health, education and skills (Skills Data Space), mobility, agriculture, energy and industry. SAMT-BU is directly affected: Skills Data Space, which the application explicitly refers to, is the European data space's answer to the need to share education and competence data across national borders – and it is the architecture SAMT-BU must be able to connect to.

**DSSC Blueprint as reference architecture.** The Data Spaces Support Centre (DSSC), EU-funded, maintains the [Blueprint for Data Spaces](https://blueprint.dssc.eu/) – the authoritative reference architecture for European data spaces. Blueprint V3.0 organises technical capabilities into three pillars: *Data Interoperability* (shared data models, semantics and exchange protocols), *Data Sovereignty and Trust* (identity, trust frameworks and policy enforcement) and *Data Value Creation Enablers* (catalogue discovery, data services and value chains). Each of these corresponds directly to concepts we use in the concept: information plane/knowledge plane, access control and data product contracts, and catalogue infrastructure.

**The relationship with the data-centric paradigm.** What is striking about the Blueprint architecture is that its technical foundation is the data-centric paradigm: RDF/OWL as knowledge representation, ODRL for rights expressions against datasets, DCAT-AP for catalogues, and R2RML/RML for mapping existing data sources to the semantic layer. The Dataspace Protocol (DSP) operationalises the principle that data remains with the owner while contracts and rights govern access. SAMT-BU is not choosing a Norwegian special variant of data-centric architecture – we are choosing the same technological direction that the EU data space ecosystem builds on. This is what makes international compatibility something other than retrofitting: we are compatible because we build on a common foundation, not because we map ourselves to it afterwards.

**DSSC Standards Landscape Update.** DSSC regularly publishes a [Standards Landscape Update](https://dssc.eu/space/SE1/185794561/) (version 1.0, January 2026) that maps the standardisation status and gaps in European data spaces. The document is a useful ongoing reference for the architecture group, but is a status report rather than a normative standard. The standards most relevant to the data-centric paradigm are dealt with concretely in 6.6 below.

### 6.3 MIMs Plus as an operational framework

**MIMs Plus** (Minimal Interoperability Mechanisms) is the operational interoperability framework for public services in cities and municipalities, EU-funded and built on the **ITU Y.4505** standard. For each mechanism area, the framework specifies: objective, capability, requirements, mechanism, interoperability guidance, and conformance testing.

MIMs Plus is structured in two layers:

**Foundational MIMs** cover the basic data flow:

- MIM0: Accessing Data – APIs to data sources
- MIM1: Interlinking Data – persistent, unique identifiers that allow entities to be traced across systems
- MIM2: Representing Data – shared data models and ontologies
- MIM3: Exchanging Data – governance models, contracts and discovery in data ecosystems
- MIM6: Securing Data – security requirements and authentication

**Application-specific MIMs** address specific domains and build on the foundational ones:

- MIM4: Personal Data – personal data management and consent
- MIM5: Interoperable AI – interoperating AI systems
- MIM7: Geospatial Data – geographic information
- MIM8: Local Digital Twins – digital twins at the local level

The most important thing for SAMT-BU is that MIMs Plus is **operational and not just regulatory**: it names concrete standards, describes how capabilities are to be realised, and is practically applicable in the pilots. It is the piece that binds regulatory frameworks (SDGR, Data Act, AI Act) to actual technical choices.

### 6.4 Mapping the requirements against MIMs Plus

The requirements we formulated in the concept choice section are not ad hoc, but are found again in MIMs Plus. The following mapping shows the relationship:

| Our requirement (section 3) | Primary MIM support | What the MIM contributes |
|---|---|---|
| 1. Data is accessed where it is owned | MIM0, MIM3 | API access to data sources; data ecosystem with federated ownership |
| 2. Semantic interoperability | MIM1, MIM2 | Persistent entity identifiers; shared data models with explicit semantics |
| 3. Gradual extension without breakage | MIM2 | Standardised, extensible data models |
| 4. International interaction | The entire MIMs framework | Concrete standard choices agreed at EU level |
| 5. AI accountability | MIM5 (forthcoming), MIM1, MIM2 | Semantic foundation that allows AI answers to be anchored in authoritative concepts |
| 6. Shared concepts for user journeys | MIM1, MIM2 | Shared vocabularies that allow services to be combined across |
| Cross-cutting | MIM6 | Security and authentication for all data access |

<br>

The mapping shows that our concept choice does not compete with MIMs Plus – it operationalises it. When we recommend "data-centric architecture with a virtual knowledge graph and layered ontology", it is a concretisation of how MIMs 1 and 2 can be realised coherently at Norwegian public-sector scale.

### 6.5 Application-specific MIMs that are particularly relevant for SAMT-BU

Three of the domain-specific MIMs are directly relevant to the project's pilots:

**MIM4 – Personal Data.** The area of children and young people largely concerns sensitive personal data and consents. MIM4 addresses personal data management, consent and connection to future EU-registered personal data intermediaries (including the EUDI Wallet). MIM4 is currently "under development" in the MIMs Plus framework, but the direction coincides with Sikt's and Digdir's ongoing work on digital wallets and consent solutions.

**MIM5 – Interoperable AI.** AI agents that are to help citizens, parents or caseworkers in SAMT-BU's domain must be able to answer accountably. MIM5 constitutes the semantic foundation for AI agents to be able to refer to authoritative concepts, sources and regulations. The semantic richness we argue for is what MIM5 presupposes in an advanced way.

**MIM7 – Geospatial Data.** User journeys in education are often geographically anchored: school catchment areas, municipal boundaries, regional division, INSPIRE obligations. MIM7 explicitly recommends OGC standards (API Features, SensorThings API) and INSPIRE conformance, which are already established in Norwegian geodata management through Geonorge.

MIM8 (Local Digital Twins) lies somewhat more to the side of the core area, but may become relevant for municipal service interfaces, youth clubs, and analogous user contexts in the longer term.

### 6.6 Key standards for the target architecture

MIMs Plus names concrete standards under MIM2. The following are particularly relevant for SAMT-BU, sorted by what they help with:

**For public services and procedures:**

- **CPSV-AP** (Core Public Service Vocabulary Application Profile) – the basis for the SDG catalogue and corresponding service descriptions. RDF-based. Relevant for the project's common service catalogue (Product 2).
- **CCCEV** (Core Criterion and Core Evidence Vocabulary) – used in OOTS evidence exchange. Relevant for diplomas, proof of competence and documentation across the public administration.

**For base data about actors:**

- **Core Person Vocabulary**, **Core Business Vocabulary**, **Core Organization Vocabulary**, **Core Location Vocabulary** – minimum vocabularies for persons, businesses, organisations and locations. RDF-based. Suitable as anchor points for Norwegian core concepts in the layered ontology.

**For data catalogues:**

- **DCAT-AP** and the Norwegian profile **DCAT-AP-NO** – already established in the National Data Catalogue on data.norge.no. Our data catalogue extension (Product 2) builds on this foundation.

**For geographic information:**

- **INSPIRE Directive** – already applicable to Norwegian geodata through Geonorge.
- **OGC API Features**, **OGC SensorThings API**, **GeoJSON**, **CityJSON** – recommended technical standards.
- **ISO/IEC 5087 City Data Model** – relevant for municipal data modelling in the longer term.

**For domain-specific extensions:**

- **SAREF / SAREF4Cities** – more relevant for IoT and smart cities than for SAMT-BU's core area, but useful for the connection to other municipal data.
- **NGSI-LD** – generic context information model, most relevant where real-time data is part of the service composition.

For the education domain specifically, we recommend that the architecture group also considers **PROV-O** (the W3C-recommended provenance vocabulary for tracing the origin and processing of data) and **ODRL** (Open Digital Rights Language for expressing terms of use), both of which are mentioned by Gioia and used in modern data product architectures.

**For data space connection and semantic foundation (DSSC Blueprint):**

- **RDF/RDFS/OWL** – the trinity of W3C standards that is the Blueprint architecture's knowledge representation layer. RDF describes the graph; RDFS and OWL define vocabulary and ontology properties. These are the foundation for the entire semantic layer in the concept – it is no coincidence that the Blueprint explicitly highlights them as the foundation.
- **[SHACL](#shacl)** (Shapes Constraint Language) – used to validate that RDF graphs conform to ontology requirements: cardinality, data types, permitted values. A necessary governance tool when the ontology is managed by a federated team and different actors deliver data against it.
- **Dataspace Protocol (DSP)** – specifies how DCAT catalogues, ODRL policies and data transfer agreements are coordinated between connectors in a data space. It is DSP that operationalises "data remains with the owner" in the Blueprint architecture, and it is the protocol Skills Data Space uses for cross-border data sharing.
- **[LDES](#ldes)** (Linked Data Event Streams) – W3C specification for publishing and consuming datasets as evolving streams according to Linked Data principles. Relevant where authoritative sources are continuously updated (for example event streams from the National Population Register or a school register) and consumers need to keep their local state synchronised without a full reload.

### 6.7 The relationship with Norwegian infrastructure and ongoing work

Several Norwegian initiatives are already closely aligned with the EU framework and should be seen in context:

- **The National Data Catalogue (data.norge.no)** is DCAT-AP-NO-based. It is the natural place for SAMT-BU's extensions under Product 2.
- **Sikt's work on the education register and the register of proof of competence** is already oriented towards CCCEV-compatible evidence models, in particular through the Europass Digital Credentials Framework.
- **EUDI Wallet** (Digdir leads the Norwegian implementation) is the natural carrier for digital diplomas and proof of competence from Sikt's registers.
- **Skills Data Space** (EU initiative, explicitly mentioned in the application) is the European data space platform where Norwegian education data can be exposed according to data-centric architecture and shared vocabularies.
- **The KS Fiks platform** and **Novari's FINT** are national components that should over time evaluate a transition towards semantically based models, in particular in areas where cross-sector sharing is central.

The concept description does not hold that all of these should be changed. It holds that the *direction* should be consistent: new solutions and extensions should build on the semantic foundation, and existing components should be gradually adapted where there is need and cost-benefit.

### 6.8 The "minimum-plus" position

There is one important nuance to be explicit about. MIMs Plus is deliberately formulated as *"minimal but sufficient"* interoperability. It is a baseline framework so that cities and municipalities can get started without investing in full-scale semantic infrastructure from day one.

Our concept choice goes beyond the MIMs Plus baseline. Data-centric service development with a virtual knowledge graph and layered ontology requires more semantic maturity than the MIMs Plus minimum requirements demand. McComb and Gioia push in the same direction – towards richer semantics, explicit ontologies at several levels, and data-product-oriented organisation.

We defend this "minimum-plus" position as follows:

- *The MIMs Plus baseline is our lower limit.* Everything we do shall be compatible with the framework, so that the Norwegian public sector can readily interact with European partners.
- *Data-centric + knowledge graph is our direction beyond the baseline.* We aim at what MIMs Plus itself points to as "future-proof" interoperability, and what Gioia's logical knowledge warehouse architecture describes as a realistic goal for modern data-centric organisations.
- *We build gradually.* We do not require the entire ecosystem to be at the "plus" level from day one. We require the direction to be consistent, so that investments build upwards and do not need to be redone.

The practical consequence is: all MVPs and pilots shall as a minimum satisfy the MIMs Plus baseline (foundational MIMs 0–3 and 6 where relevant), and they shall demonstrate how the baseline can be extended with knowledge graph properties for the domains where it adds value.

### 6.9 What has not been clarified

Three matters lie outside what this concept description can decide, and must be assessed by the architecture group:

- **The relationship between NGSI-LD and a more general RDF approach.** NGSI-LD is strongly anchored in smart cities (the FIWARE ecosystem) and has its own APIs. For SAMT-BU's domain it is not obvious that NGSI-LD is the right choice everywhere – it may be more correct to use pure RDF/SPARQL with JSON-LD fronts for education data, and NGSI-LD where real-time and IoT data are involved. This is a target architecture choice.
- **Which upper ontology** (BFO, GIST, or a pragmatic variant of these) is to be recommended for the Norwegian public domain. Gioia proposes the standards; it is a real choice for the architecture group.
- **Implementation stack for the virtual knowledge graph.** Triplestores, virtual graph engines, R2RML/RML mapping, or alternative property graph solutions are technology choices that belong to the target architecture.

These are real open questions, not rhetorical ones. The concept description commits the semantic direction; it lets the architecture group decide which stack realises it.

---

## 7. Implications

The concept in this description has consequences that reach beyond the architectural core. This section gathers the most important ones, so that the architecture group and the pilots have a clear picture of what the concept choice means in practice.

### 7.1 Data-centric is the means, data-driven is the goal

The application uses the term "data-driven service development" as the overall aim. This concept description is not a competitor to that phrase – it is a clarification of *how* data-driven service development is to be possible at public-sector scale.

"Data-driven" describes the aim: services and decisions based on data of good quality. "Data-centric" describes the architectural discipline that makes it realistic: data, with shared explicit meaning, is what is stable, and applications are replaceable projections. Without the architectural discipline, "data-driven" becomes an aspiration we repeat without achieving.

The relationship is means to end, not alternative paradigms. The concept description commits to data-centric architecture as the operational means of achieving data-driven service delivery.

### 7.2 User-oriented data products

In the concept description we have taken an explicit position that applications – including AI agents – are consumers, not owners of data (4.3.4). That is one side of data product orientation: that data is delivered as products with clear stewardship responsibility, contracts and semantic annotation.

There is another side that is equally important for the public sector: that the data products must understand and relate to the *end users* of the services that rest on them. In the private sector there is an open discussion about whether data product owners should isolate themselves from end users for reasons of scalability. For the public sector that discussion is settled: we are there for citizens, parents, pupils, teachers and caseworkers. The data products must therefore be service- and user-journey-oriented, not just efficient technical data deliveries.

In practice, this means that:

- Data products must be described in a language that consumers across professional domains understand – not only for other data engineers
- The contracts must address real usage needs from services, not just technical interface specifications
- Data product owners must have a relationship with those who deliver services to end users, not isolate themselves for reasons of scalability

This is a Norwegian public-sector clarification of data product orientation, not a competitor to it.

### 7.3 AI and accountability

AI agents are becoming an increasingly important part of public service delivery. The concept description presupposes that this happens in a responsible way: that the agents base their answers and actions on authoritative data, and that their answers can be verified.

Data-centric architecture with a virtual knowledge graph is the prerequisite for this to be possible:

- AI agents retrieve facts from authoritative sources through the semantic layer – not from their own training data or local knowledge stores
- The answers from an agent can be traced back to the source through semantic references
- The concepts the agent uses are anchored in a shared ontology, not in the agent's own interpretations

This is consistent with approaches such as *GraphRAG* (Retrieval-Augmented Generation extended with a knowledge graph) and *neuro-symbolic AI* (the combination of neural models and symbolic knowledge representation). This is not academic theory – it is the professional direction serious actors in responsible AI in the public sector are moving towards.

The concept description is probably the only architectural direction that allows the public sector to integrate AI agents without repeating the mistakes of the first generation of line-of-business systems: new locked-in systems with their own data models and no connection with the rest.

### 7.4 Gradual realisation of value

Another implication is that the concept does not presuppose one big completion before value can be realised. The semantic knowledge graph's property of monotonic growth (4.5) means that:

- Each pilot can deliver value in its own context, while extending the foundation for the next pilot
- Existing line-of-business systems can be connected gradually, according to priority and need
- The semantic foundation is built up domain by domain, not as one big modelling effort in advance

This has consequences for how the project's pilots and MVPs should be designed: each pilot should not only solve its immediate user problem, but also contribute concretely to the semantic foundation – new concepts, new relationships, new data product annotations. The pilots are not trial balloons; they are building blocks in an accumulating infrastructure.

### 7.5 Prerequisite of a federated modelling structure

The concept description presupposes that a **federated modelling structure** (4.2) is established in which representatives from the sectors involved have a mandate to manage the shared concepts – in particular the domain ontology that is shared across. This is not an organisational model we specify here; composition, governance and decision mechanisms belong to the project's organisational work and to SKATE/the joint governance structure.

It is nevertheless worth flagging that such a structure is necessary for the concept to be realised operationally. Without a body with a mandate to manage shared concepts across sectors, the knowledge graph becomes a fragmented set of isolated subdomains – and we recreate the coordination problem we are trying to solve. This is one of the most important organisational consequences of the concept choice.

---

## 8. Scope and open questions

This section makes explicit where the concept description ends. A concept description that is not clear about its own limits invites being read as more – or less – than it is. Here we draw the line between what the concept commits to and what belongs to the architecture group's further work, the target architecture and the pilots. We gather the open questions that are real, not rhetorical, and we conclude with the strongest objection to the concept choice – because a concept description that cannot withstand its own opposition has not been fully thought through.

### 8.1 Concept, not solution – where the line goes

The concept description stands at *concept level*. It commits to a paradigmatic direction – data-centric service development – and to an architectural pattern – a virtual, layered knowledge graph with federated ontology and data product orientation. It does **not** commit to concrete technology choices, products, suppliers, storage solutions, modelling tools or infrastructure set-ups.

This distinction is worth being explicit about, because the concept may be met with the objection that we are already at solution level when we say "virtual knowledge graph". We are not. "Virtual knowledge graph" names a *pattern* – data remains with its sources, the semantics lives in a shared ontology, and consumers access data through the semantic layer – not an implementation. The question of RDF or property graph, SPARQL or Cypher, triplestore or virtual graph engine, R2RML or RML, are precisely the choices the concept does *not* make. They belong in the target architecture.

We thus have two tools against the objection that we confuse concept and solution: we *have* made a reasoned concept choice (section 3), and we *stay* at concept level and are explicit about where the line goes (this section). It is a deliberate division of labour, not an omission.

### 8.2 What is left to the target architecture and the architecture group

The following are real open questions that the concept description deliberately leaves open:

- **Implementation stack.** Triplestores, virtual graph engines, mapping engines (R2RML/RML) or property-graph-based solutions are technology choices for the target architecture. Elaborated in 6.9.
- **Choice of upper ontology.** BFO, GIST or a pragmatic variant – the standards exist, but the choice for the Norwegian public domain is the architecture group's (6.9).
- **NGSI-LD versus a more general RDF approach.** Probably RDF/SPARQL with JSON-LD fronts for education data, and NGSI-LD where real-time and IoT data are involved – but this is a target architecture choice (6.9).
- **Identifier strategy.** Which persistent, unique identifiers are to bind entities together across (MIM1), and how they relate to existing national identifiers, is not clarified here.
- **Management of the mapping layer.** How the mappings between data sources and ontology (R2RML/RML) are to be versioned, tested and owned operationally is a target architecture and operations matter.
- **Degree of materialisation over time.** The concept starts virtual. When and whether certain parts should be materialised – referenced data can be materialised later, but not the other way round (4.1) – is a roadmap question, not a concept choice.
- **Enforcement of access control.** Rights expressed against datasets ([ODRL](#odrl)) must be enforceable by machine against concrete requests, typically by being mapped to an enforcement framework ([XACML](#xacml) with PEP/PDP). The choice of profile and architecture is a target architecture matter.
- **National access infrastructure.** [Altinn Autorisasjon](#altinn-autorisasjon)'s resource registry is currently oriented towards services and APIs, not towards datasets: there is no resource type for datasets, and the ID format does not allow IRIs. The architecture is resource-based and extensible, so this is not an obstacle in principle – but it is a national infrastructure gap that must be addressed for data-centric access control to be realised in practice.

This also includes the **current situation and positioning against established predecessors**. A thorough mapping of existing line-of-business systems, data management and collaboration patterns in the affected sectors – and a precise assessment of how SAMT-BU relates to efforts such as FINT, KUDAF and the FIKS platform – is part of the architecture group's own work, not this concept description's. What we have said about the predecessors is kept to what is necessary: FINT is assessed as alternative C in the concept choice (section 3), and the connection to ongoing national work is outlined in section 6. The full positioning requires a description of the current situation that belongs in the architecture work.

One access problem is solved neither by the concept nor by the established European frameworks we anchor ourselves in (6.2), and should be flagged explicitly. When an API can return different data depending on context – a SPARQL endpoint or a query-based API over the knowledge graph – access control is no longer a question of allowing or refusing a call, but of filtering the response so that the consumer only sees what she is entitled to. The gap is documented: [IDSA's Dataspace Protocol](#idsa-dataspace-protocol) and the [DSSC Blueprint](#dssc-blueprint) define access at dataset level, but leave enforcement to the connector; [SIMPL's](#simpl) Policy Filter Service filters which resources are returned in a catalogue search according to the user's rights, but does not address filtering of the content of the individual dataset; and [Catena-X's Knowledge Agents (CX-0084)](#catena-x-knowledge-agents-cx-0084) opens up row- and attribute-level access as a possibility, not a specified mechanism. For SAMT-BU this is not an edge case: the domain combines information of very different sensitivity – health, school results, social circumstances – which may be touched by the same query. Until patterns for such filtering are standardised, the data product itself (or the binding layer in a knowledge graph) must carry the logic; the safest approach today is separate, pre-annotated distributions with their own policies for different levels of access rather than dynamic filtering of one endpoint. The need should be reported to the European standardisation and community channels (DSSC, IDSA), where Digdir can raise it as a requirement from the public sector.

### 8.3 Organisational and governance open questions

The concept presupposes a federated modelling structure (4.2, 7.5), but does not specify it. The open questions here are probably the ones that decide whether the concept succeeds in practice:

- Who owns the domain ontology – the layer that by definition is shared across sectors?
- Which body has the mandate to decide when a core concept is to be specialised, and to resolve conflicts when two sectors model the same concept differently?
- How does the modelling structure relate to existing joint governance (SKATE) and to the partners' own lines of governance?

These are stewardship and governance questions disguised as technical ones. Experience from similar work is that the biggest brake is rarely the technology, but the coordination: who has the authority to commit whom. The concept description flags the need; it does not solve it.

### 8.4 Legal and data protection clarifications

SAMT-BU's domain – children and young people – involves extensive processing of sensitive personal data. The concept describes an architecture for sharing data with shared meaning; it does not decide *when* such sharing is lawful. The following clarifications lie outside the concept description, but the concept's feasibility depends on them, and they should be followed closely by the project's legal workstream and the architecture group:

- **Legal basis versus consent** for sharing across sectors, and the relationship with data minimisation. The distinction between the three forms of "ownership" (4.3.1) is an architectural contribution to this discussion, not a legal conclusion.
- **The EU AI Act.** The obligations for high-risk AI under Annex III were, through the Digital Omnibus agreement in May 2026, postponed from August 2026 to December 2027 – roughly coinciding with the end of the project. Public bodies that put such systems into use nonetheless get registration and impact assessment obligations. The AI agents the concept describes (4.3.4, 7.3) must be designed with this in mind.
- **Digital wallets.** The EUDI Wallet, which is the operational carrier of the data subject's control in the concept (4.3.1), has for EEA countries including Norway a deadline towards the end of 2027, and in early 2026 had not yet been put into operation or certified anywhere. The concept presupposes wallets as maturity-dependent infrastructure, not as something finished that exists today.

### 8.5 Related concept descriptions that should follow

This concept description is the first in a chain. It commits the direction; several concepts need their own clarification before the target architecture can be fully built out. In the order we see it:

- **Knowledge graph** – the realisation as a separate concept, where the technical choices 8.2 leaves open can be discussed on their own terms.
- **Shared conceptual apparatus / core concepts** – the human interface to the domain ontology.
- **Data virtualisation** – the technique for exposing the graph to the applications without moving data.
- **Data product orientation** – the organisational structure with contracts, ownership and federated governance.
- **User journeys and service composition** – how coherent services are assembled on top of the semantic infrastructure.

Possibly also a separate clarification of **semantic interoperability**, which can borrow a lot from Digdir's established definition. Each of these can be written when a concrete need requires it – the same principle that governs the modelling in the concept itself.

### 8.6 The strongest objection to the concept

A concept description becomes more credible, not less, by taking its own opposition seriously. The strongest objection to the concept choice is this:

Semantic web technologies are more than twenty years old, and broad adoption has failed to materialise outside limited pockets. The approach is regularly criticised for being too academic, and broad impact has come via *lightweight* variants – Schema.org, Linked Open Data, JSON-LD as a thin semantic layer on REST – not via formal, layered ontologies. Top-level ontologies such as BFO and DOLCE have been available all along without becoming the foundation in the public sector anywhere. Pragmatic alternatives – API-first with lightweight shared vocabularies, or data products with contract-based interfaces and minimal semantic glue – often deliver most of the interoperability value at a fraction of the cost. The risk of over-engineering is real: one may end up building a cathedral while others build working villages.

The objection deserves an honest answer, and the answer has two parts.

First, it mainly concerns *level of ambition and pace*, not direction. None of the lightweight alternatives has actually demonstrated what SAMT-BU is aiming for: coherent services across sectors *and* national borders, with machine-understandable regulations and automated reasoning over data. They scale well for open data and simple integrations, but creak when one has to *reason* over the data. If one holds on to the ambition of coherent services with the user at the centre, we have not seen a real alternative to a semantic layer at the bottom.

Second, it follows that the concept choice should not be sold as technically inevitable. It is the best documented choice *given the ambition* – not a logical necessity. If the ambition is lowered, alternative paths open up. This is a more honest and more tenable position than claiming that there are no other paths, and it is the reason why the concept description has consistently chosen wordings such as "the most robust approach we know" rather than "the only feasible path".

The practical consequence of taking the objection seriously is the gradual approach the concept already commits to (4.5): we build semantic maturity where the ambition requires it and the value is greatest, not everywhere at once. This is precisely how one avoids the cathedral without giving up the coherence.

---

## 9. References

This document builds on a small set of sources. The literature explains the paradigm and the architectural structure the concept rests on; the standards and frameworks are the operational references the concept is anchored in. References in the running text point here.

### Literature

#### McComb (2018)

Dave McComb: *Software Wasteland: How the Application-Centric Mindset is Hobbling our Enterprises.* Technics Publications, 2018. The argument that the application-centric mindset is in itself a main source of cost and complexity in organisations' information systems.

#### McComb (2019)

Dave McComb: *The Data-Centric Revolution: Restoring Sanity to Enterprise Information Systems.* Technics Publications, 2019. The central presentation of the data-centric paradigm – "single but federated", the relationship with the relational model, and the knowledge graph as architectural foundation.

#### Gioia (2024)

Andrea Gioia: *Managing Data as a Product: A practical guide to enterprise data management.* Packt Publishing, November 2024. ISBN 978-1-83546-853-1. Source of the data product orientation, the layered ontology, the three knowledge graph architectures and the four-part information architecture plane (chapter 11).

### Standards and frameworks

#### MIMs Plus

Minimal Interoperability Mechanisms Plus – Living-in.EU / OASC. The EU's operational interoperability mechanisms, revised annually. <https://living-in.eu/>

#### SEMIC Core Vocabularies

Simplified, reusable core models for, among other things, person, business and location – Interoperable Europe (European Commission). <https://interoperable-europe.ec.europa.eu/collection/semic-support-centre/core-vocabularies>

#### DCAT-AP-NO

The Norwegian application profile of DCAT-AP for describing datasets and data services – Digdir. <https://data.norge.no/specification/dcat-ap-no>

#### DPDS

Data Product Descriptor Specification – Open Data Mesh Initiative. Standardised description of data products, including semantic links to the ontology. <https://dpds.opendatamesh.org/>

#### R2RML and RML

Standard languages for mapping relational data and semi-structured data, respectively, to RDF – W3C. <https://www.w3.org/TR/r2rml/> · <https://rml.io/>

#### RDF and SPARQL

The basic standards for representing and querying graph data – W3C. <https://www.w3.org/TR/rdf11-concepts/> · <https://www.w3.org/TR/sparql11-query/>

#### GIST

Pragmatic upper ontology developed for enterprises – Semantic Arts. <https://www.semanticarts.com/gist/>

#### BFO

Basic Formal Ontology, a formal upper ontology – ISO/IEC 21838-2:2021. <https://basic-formal-ontology.org/>

#### Digdir

Framework for digital interaction and the definition of semantic interoperability – the Norwegian Digitalisation Agency. <https://www.digdir.no/>

#### ODRL

Open Digital Rights Language – W3C. Policy language for expressing terms of use and access rights against resources such as datasets. <https://www.w3.org/TR/odrl-model/>

#### XACML

eXtensible Access Control Markup Language – OASIS. Framework for evaluating and enforcing access policies (PEP/PDP/PIP/PAP). <https://docs.oasis-open.org/xacml/3.0/xacml-3.0-core-spec-os-en.html>

#### IDSA Dataspace Protocol

Protocol for data sharing between connectors in data spaces – International Data Spaces Association. <https://kb.internationaldataspaces.org/>

#### DSSC Blueprint

Common reference architecture for European data spaces – Data Spaces Support Centre. <https://blueprint.dssc.eu/>

#### Catena-X Knowledge Agents (CX-0084)

Standard for federated queries in data spaces (compute-to-data over a knowledge graph) – Catena-X. <https://catenax-ev.github.io/docs/next/standards/CX-0084-FederatedQueriesInDataSpaces>

#### SIMPL

The EU's middleware platform for European data spaces – European Commission. Policy Filter Service described in Functional and Technical Architecture Specifications §9.2.5. <https://digital-strategy.ec.europa.eu/en/policies/simpl>

#### Altinn Autorisasjon

National access control and resource registry infrastructure – Digdir/Altinn. <https://docs.altinn.studio/authorization/>

#### SHACL

Shapes Constraint Language – W3C. Validates that RDF graphs conform to ontology requirements (cardinality, data types, permitted values). <https://www.w3.org/TR/shacl/>

#### LDES

Linked Data Event Streams – W3C Community Group. Publishes and consumes evolving datasets as streams according to Linked Data principles. <https://w3id.org/ldes/specification>

### Legislation

*This subsection is under development. The picture below is not complete and will change as new legislation enters into force and Norwegian implementation is clarified.*

Digdir maintains an ongoing [overview of EU legislation on the sharing and use of data](https://www.digdir.no/datadeling/oversikt-over-eu-regelverk-om-deling-og-bruk-av-data/3251) that is relevant to the Norwegian public sector. At the time of this concept description, the overview covers ten regulations and directives, grouped in two layers: four core acts that directly regulate data protection and data sharing – the **GDPR** (General Data Protection Regulation), the **Open Data Directive** (ODD), the **Data Governance Act** (DGA) and the **Data Act** – and six adjacent pieces of legislation: the AI Act, eIDAS, Single Digital Gateway (SDG), Digital Markets Act (DMA), Digital Services Act (DSA) and Interoperable Europe Act. Note that Digdir links have historically become invalid when the website is updated – search for the title if the link is broken.

Beyond EU legislation, sector-specific Norwegian acts are directly relevant to SAMT-BU's domain: the Patient Records Act, the Health Registry Act, the Education Act and the Child Welfare Act regulate which data may be processed and shared, and on what conditions. These, as well as any new legal bases that follow from the project's work, will be added over time.

#### EU AI Act

Regulation (EU) 2024/1689. The obligations for high-risk AI under Annex III were, through the Digital Omnibus agreement in May 2026, postponed to December 2027. <https://eur-lex.europa.eu/eli/reg/2024/1689/oj> · <https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai>

#### EUDI Wallet

The European Digital Identity Wallet under eIDAS 2 (Regulation (EU) 2024/1183). For EEA countries including Norway, a deadline towards the end of 2027 applies. <https://digital-strategy.ec.europa.eu/en/policies/eudi-wallet-implementation>
