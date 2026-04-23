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
        ┌─────────────────┬───┴───┬─────────────────┐
        ▼                 ▼       ▼                 ▼
      Neo4j        FollowTheMoney  GQL        Linked Data (RDF)
        │                 │       │                 │
        ▼                 ▼       ▼                 ▼
  Graph queries   Sanctions data BigQuery   Knowledge graphs
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

- **BODS Validator** — [github.com/StephenAbbott/bods-validator](https://github.com/StephenAbbott/bods-validator) — schema and content checks against the published standard
- **BODS Forms** — [github.com/StephenAbbott/bods-forms](https://github.com/StephenAbbott/bods-forms)

### Conversion & interoperability

- **Neo4j integration** — [github.com/StephenAbbott/bods-neo4j](https://github.com/StephenAbbott/bods-neo4j) — load BODS into a property graph for ownership queries
- **FollowTheMoney** — [github.com/StephenAbbott/bods-ftm](https://github.com/StephenAbbott/bods-ftm)
- **GQL / BigQuery** — [github.com/StephenAbbott/bods-gql](https://github.com/StephenAbbott/bods-gql)
- **BODS XML** — [github.com/StephenAbbott/bods-xml](https://github.com/StephenAbbott/bods-xml)
- **BODS Lance** — [github.com/StephenAbbott/bods-lance](https://github.com/StephenAbbott/bods-lance)

### External ecosystem tools

- **bodsdata** — [github.com/openownership/bodsdata](https://github.com/openownership/bodsdata)
- **RDF vocabulary** — [github.com/openownership/bodsld](https://github.com/openownership/bodsld)

### AI & skills

- [github.com/StephenAbbott/beneficial-ownership-data](https://github.com/StephenAbbott/beneficial-ownership-data)
- [github.com/StephenAbbott/bods-skill](https://github.com/StephenAbbott/bods-skill)

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
