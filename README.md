# BODS Interoperability Toolkit

**Practical tools and workflows for validating, transforming, and using Beneficial Ownership Data Standard (BODS) data across real-world systems.**

This repository brings together tools, mappings, and implementation patterns that make BODS data usable in:

- Registry systems
- Procurement and anti-corruption workflows
- AML / compliance pipelines
- Investigative and OSINT analysis
- Graph and linked data environments

---

## 🚀 Start here

What do you want to do?

- [Validate BODS data](WORKFLOWS/validate-bods-data.md)
- [Convert BODS into usable formats](WORKFLOWS/convert-bods-data.md)
- [Analyse ownership networks](WORKFLOWS/analyse-ownership-networks.md)
- [Integrate BODS into an existing system](WORKFLOWS/integrate-with-external-systems.md)

Not sure which tool fits? See the [tool decision tree](DECISION-TREES/choose-your-tool.md).

---

## 🧭 Choose your workflow

| If you want to… | Go here |
|----------------|--------|
| Validate BODS data | [WORKFLOWS/validate-bods-data.md](WORKFLOWS/validate-bods-data.md) |
| Convert BODS into other formats | [WORKFLOWS/convert-bods-data.md](WORKFLOWS/convert-bods-data.md) |
| Analyse ownership networks | [WORKFLOWS/analyse-ownership-networks.md](WORKFLOWS/analyse-ownership-networks.md) |
| Integrate BODS into systems | [WORKFLOWS/integrate-with-external-systems.md](WORKFLOWS/integrate-with-external-systems.md) |

---

## 🏗 Architecture overview

```
                                  [ BODS JSON ]
                                        │
                                        ▼
                                  [ Validation ]
                                        │
         ┌──────────────────┬───────────┴──────────┬──────────────────┐
         ▼                  ▼                      ▼                  ▼
       Neo4j         FollowTheMoney               GQL         Linked Data (RDF)
         │                  │                      │                  │
         ▼                  ▼                      ▼                  ▼
   Graph queries     Sanctions data            BigQuery        Knowledge graphs
```

BODS acts as an **interoperability layer** between beneficial ownership data and downstream systems.

---

## 👥 Who this is for

- Registry implementers
- Procurement / anti-corruption practitioners
- AML / compliance engineers
- Data journalists / investigators
- Developers working with structured ownership data

---

## 🔧 Tools

### Core validation & interaction

- **BODS Validator** — [github.com/StephenAbbott/bods-validator](https://github.com/StephenAbbott/bods-validator) — validate and visualise beneficial ownership data against version 0.4 of the BODS schema
- **BODS Forms** — [github.com/StephenAbbott/bods-forms](https://github.com/StephenAbbott/bods-forms) — user-friendly form that produces valid data in line with BODS v0.4
- **BODS Fixtures** — [github.com/StephenAbbott/bods-fixtures](https://github.com/StephenAbbott/bods-fixtures) — canonical BODS v0.4 fixture pack for testing BODS adapters
- **pytest-bods-fixtures** — [github.com/StephenAbbott/pytest-bods-fixtures](https://github.com/StephenAbbott/pytest-bods-fixtures) — pytest plugin: parametrised fixture over the canonical bods-fixtures v0.4 conformance pack

### Conversion & interoperability

- **Neo4j integration** — [github.com/StephenAbbott/bods-neo4j](https://github.com/StephenAbbott/bods-neo4j) — bidirectional converter between BODS v0.4 and Neo4j, with UBO detection, corporate group mapping, and circular ownership analysis
- **FollowTheMoney** — [github.com/StephenAbbott/bods-ftm](https://github.com/StephenAbbott/bods-ftm) — bidirectional converter between BODS v0.4 and the FollowTheMoney data model used by OpenSanctions, OpenAleph and others
- **GQL / BigQuery** — [github.com/StephenAbbott/bods-gql](https://github.com/StephenAbbott/bods-gql) — convert BODS v0.4 data for querying with GQL (ISO/IEC 39075) on BigQuery
- **BODS XML** — [github.com/StephenAbbott/bods-xml](https://github.com/StephenAbbott/bods-xml) — convert BODS v0.4 JSON to XML
- **BODS Lance** — [github.com/StephenAbbott/bods-lance](https://github.com/StephenAbbott/bods-lance) — convert BODS v0.4 data to the Lance columnar format
- **BODS ↔ AML AI** — [github.com/StephenAbbott/bods-aml-ai](https://github.com/StephenAbbott/bods-aml-ai) — transform BODS v0.4 data into Google Anti Money Laundering AI input format
- **BODS ↔ ICIJ Offshore Leaks** — [github.com/StephenAbbott/bods-icij-offshoreleaks](https://github.com/StephenAbbott/bods-icij-offshoreleaks) — transform ICIJ Offshore Leaks Database records into BODS v0.4, with Neo4j export support
- **BODS ↔ OpenCorporates** — [github.com/StephenAbbott/bods-opencorporates](https://github.com/StephenAbbott/bods-opencorporates) — transform OpenCorporates relationship data into BODS v0.4
- **BODS ↔ BrightQuery** — [github.com/StephenAbbott/bods-brightquery](https://github.com/StephenAbbott/bods-brightquery) — transform BrightQuery's corporate ownership data from opendata.org into BODS v0.4
- **BODS ↔ Kyckr** — [github.com/StephenAbbott/bods-kyckr](https://github.com/StephenAbbott/bods-kyckr) — transform Kyckr relationship data into BODS v0.4

### External ecosystem tools

- **bodsdata** — [github.com/openownership/bodsdata](https://github.com/openownership/bodsdata) — convert BODS JSON to CSV, SQLite, PostgreSQL and Parquet
- **bodsanalysis** — [github.com/openownership/bodsanalysis](https://github.com/openownership/bodsanalysis) — notebooks and code for analysing data published to the Beneficial Ownership Data Standard
- **RDF vocabulary** — [github.com/openownership/bodsld](https://github.com/openownership/bodsld) — RDF / linked data vocabulary for BODS
- **bodsriskdetection** — [github.com/openownership/bodsriskdetection](https://github.com/openownership/bodsriskdetection) — proof-of-concept demonstrating the use of BODS in an RDF format

### AI & skills

- **beneficial-ownership-data** — [github.com/StephenAbbott/beneficial-ownership-data](https://github.com/StephenAbbott/beneficial-ownership-data) — expert Claude skill for beneficial ownership data
- **bods-skill** — [github.com/StephenAbbott/bods-skill](https://github.com/StephenAbbott/bods-skill) — Claude skill providing expert reference for BODS v0.4

---

## 🔄 Key workflows

**Validate:** BODS → Validator → clean dataset

**Convert:**
- Graph → Neo4j
- Sanctions → FollowTheMoney
- Analytics → GQL / BigQuery
- Tabular → bodsdata
- Linked data → RDF

**Analyse:**
- Ownership chains
- Control structures
- Network risks

**Integrate:**
- Procurement systems
- Registries
- AML pipelines
- Knowledge graphs

---

## 🌐 Why this matters

Transforming BODS into graph, tabular, and linked data formats enables:

- AI applications
- Cross-dataset linking
- Scalable risk detection
- Real-world operational use

---

## 📚 Resources

- [Beneficial Ownership Data Standard](https://standard.openownership.org/)
- [Open Ownership](https://www.openownership.org/)
- [BODS schema reference](https://standard.openownership.org/en/latest/standard/reference.html)
- [BODS GitHub](https://github.com/openownership/data-standard)

---

## 🤝 Contributing

Contributions welcome:

- Data mappings
- Conversion tools
- Documentation
- Example datasets

Open an issue or pull request.
