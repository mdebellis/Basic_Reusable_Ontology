# Basic Reusable Ontology (BRO)

The **Basic Reusable Ontology (BRO)** is a small family of modular, practical ontologies designed for real-world knowledge engineering. Unlike many upper ontologies grounded in philosophical or psychological theories (e.g., BFO, DOLCE), BRO takes a **software-engineering** approach: start small, reuse widely adopted standards, and include only what is consistently useful across many domains.

BRO consists of **three layers**, each building on the previous one:

---

## 1. `basic_bro`
**A lightweight, reusable metadata layer.**

- Reuses selected **Dublin Core Terms** and **SKOS annotation properties**.
- All properties are **annotation properties** so they can be used on classes, properties, or individuals.
- No classes or object properties.  
- No datatypes are enforced, allowing values to be literals or IRIs.
- Intended as the “baseline vocabulary” used in nearly every ontology.

---

## 2. `bro_pro`
**Basic Bro plus a cleaned subset of PROV-O.**

- Includes the essential **PROV entities (Activity, Agent, Entity)** and core provenance properties.
- Retains the **canonical PROV IRIs**.
- Removes problematic or unnecessary elements (e.g., PROV annotation/object-property punning) to maintain OWL DL compatibility.
- Provides an extremely compact and clean PROV-based provenance layer for use in operational ontologies.

---

## 3. `big_bro`
**A larger reusable layer for domains that need shared agent and organization patterns.**

- Includes all of **Basic Bro** and the PROV subset from **Bro Pro**.
- Adds selected reusable classes commonly needed in real systems (e.g., Person, Organization, Activity patterns).
- Still intentionally small: not a full upper ontology, but a practical, real-world foundation.

---

## Design Philosophy

BRO is not intended to be an exhaustive upper ontology.  
Its goals are:

- **Practicality:** Include only what is useful across many domains.
- **Simplicity:** Keep modules small, comprehensible, and easy to adopt.
- **Reusability:** Build on widely used standards (SKOS, DCTERMS, PROV-O).
- **Experience Based:** One of my sayings regarding reuse is "to reuse you need to first use". I.e., libraries created from scratch meant to be reusable often don't provide nearly as much values as libraries created to solve real problems which are then generalized. The Bros are based on my experience building ontologies and my realization that I was starting all my new ontologies with a basic set of metadata annotation properties. 
- **Modularity:** Allow users to import only the layers they need.
- **Metadata** Many upper models completely ignore metadata. The primary focus on the Bros is on metadata and provenance

Thus, the Bro vocablaries complement rather than compete with other upper models. For more feature-rich upper ontologies, users may wish to consider:

- **Gist** (Semantic Arts)  
- **Schema.org**
- **[Simplified Upper Model Ontology](https://github.com/AIDAVA-DEV/sulo)**

BRO complements these by offering a minimal, engineering-oriented starting point.

---

## Repository Contents

- `basic_bro.ttl` — Core annotation properties
- `bro_pro.ttl` — Basic Bro + cleaned PROV subset
- `big_bro.ttl` — Higher-level reusable classes built on Bro Pro

---

## Status

Work in progress (active development).  
Feedback and suggestions are welcome.

