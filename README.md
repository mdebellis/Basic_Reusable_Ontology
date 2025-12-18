# Basic Reusable Ontology (BRO)

The **Basic Reusable Ontology (BRO)** is a small family of modular, practical ontologies
designed for real-world knowledge engineering. Unlike many upper ontologies grounded in
philosophical or psychological theories (e.g., BFO, DOLCE), BRO takes a
**software-engineering approach**: start small, reuse widely adopted standards, and
include only what is consistently useful across many domains.

BRO consists of **three layers**, each building on the previous one:

---

## 1. `basic_bro`
**A lightweight, reusable metadata layer.**

- Reuses selected **Dublin Core Terms** and **SKOS annotation properties**.
- All properties are **annotation properties**, so they can be used on classes,
  properties, or individuals.
- No classes or object properties.
- No datatypes are enforced, allowing values to be literals or IRIs.
- Intended as the **baseline vocabulary** used in nearly every ontology.

---

## 2. `big_bro`
**Reusable agent, organization, and activity patterns for real systems.**

- Includes all of **Basic Bro**.
- Adds selected reusable classes commonly needed in operational ontologies
  (e.g., Person, Organization, Activity patterns).
- Intentionally small and pragmatic: not a full upper ontology, but a shared
  foundation for many domains.

### Integration with SULO (Simplified Upper-Level Ontology)

`big_bro` incorporates selected alignments to the
**Simplified Upper-Level Ontology (SULO)**  
(<https://w3id.org/sulo/>), providing a lightweight upper-model scaffold for
commonly reused concepts such as agents, organizations, and activities.

SULO is used in `big_bro` to:

- Ground reusable classes (e.g., Person, Organization, Activity) in a
  **small, coherent upper layer**.
- Enable **cross-ontology interoperability** with other SULO-aligned models.
- Avoid reinventing high-level distinctions while remaining
  **implementation-oriented rather than philosophical**.

SULO is deliberately chosen because it shares BRO’s core design values:
simplicity, modularity, and real-world applicability. Its role in `big_bro` is
supportive rather than prescriptive—`big_bro` remains a practical foundation
ontology, not a full upper ontology.

Users who already rely on other upper models (e.g., BFO, Gist) may continue to do
so; `big_bro` is designed to **coexist** with alternative upper-level frameworks.

---

## 3. `bro_pro`
**The most complete BRO layer, adding a cleaned subset of PROV-O.**

- Includes all of **Basic Bro** and **Big Bro**.
- Adds a compact, OWL DL–safe subset of **PROV-O**, including the essential
  PROV entities (**Activity, Agent, Entity**) and core provenance properties.
- Retains the **canonical PROV IRIs**.
- Removes problematic or unnecessary elements (e.g., PROV annotation/object-property
  punning) to maintain OWL DL compatibility.
- Provides a clean, production-ready provenance layer for operational knowledge graphs.

---

## Design Philosophy

BRO is not intended to be an exhaustive upper ontology.  
Its goals are:

- **Practicality:** Include only what is useful across many domains.
- **Simplicity:** Keep modules small, comprehensible, and easy to adopt.
- **Reusability:** Build on widely used standards (SKOS, DCTERMS, PROV-O).
- **Experience-based design:** “To reuse, you need to first use.”  
  The BRO vocabularies grew out of real ontology projects and recurring needs,
  not abstract design goals.
- **Modularity:** Allow users to import only the layers they need.
- **Metadata-first:** Many upper models ignore metadata; BRO places metadata and
  provenance at its core.

Thus, the BRO vocabularies **complement rather than compete** with other upper models.
For more feature-rich upper ontologies, users may wish to consider:

- **[Gist (Semantic Arts)](https://www.semanticarts.com/gist/)**
- **[Basic Formal Ontology (BFO)](https://basic-formal-ontology.org/)**
- **Schema.org**

---

## Repository Contents

- `basic_bro.ttl` — Core annotation properties
- `big_bro.ttl` — Reusable agent and organization patterns (SULO-aligned)
- `bro_pro.ttl` — Big Bro plus a cleaned PROV-O subset

---

## Status

Work in progress (active development).  
Feedback and suggestions are welcome.
