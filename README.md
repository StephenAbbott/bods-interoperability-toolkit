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

→ Validate BODS data  
→ Convert BODS into usable formats  
→ Analyse ownership networks  
→ Integrate BODS into an existing system  

---

## 🧭 Choose your workflow

| If you want to… | Go here |
|----------------|--------|
| Validate BODS data | WORKFLOWS/validate-bods-data.md |
| Convert BODS into other formats | WORKFLOWS/convert-bods-data.md |
| Analyse ownership networks | WORKFLOWS/analyse-ownership-networks.md |
| Integrate BODS into systems | WORKFLOWS/integrate-with-external-systems.md |

---

## 🏗 Architecture overview

[BODS JSON]  
↓  
[Validation]  
↓  
├───────────────┬───────────────┬───────────────┬───────────────┐  
↓               ↓               ↓               ↓  
Neo4j         FollowTheMoney     GQL           Linked Data (RDF)  
↓               ↓               ↓               ↓  
Graph queries   Sanctions data   BigQuery       Knowledge graphs  

BODS acts as an **interoperability layer** between beneficial ownership data and downstream systems.

---

## 👥 Who this is for

- Registry implementers  
- Procurement / anti-corruption practitioners  
- AML / compliance engineers  
- Data journalists / investigators  
- Developers working with structured ownership data  

---

# 🔧 Tools

## Core validation & interaction

- BODS Validator  
- BODS Forms → https://github.com/StephenAbbott/bods-forms  

---

## Conversion & interoperability (Stephen Abbott)

- Neo4j integration  
- FollowTheMoney → https://github.com/StephenAbbott/bods-ftm  
- GQL / BigQuery → https://github.com/StephenAbbott/bods-gql  
- BODS XML → https://github.com/StephenAbbott/bods-xml  
- BODS Lance → https://github.com/StephenAbbott/bods-lance  

---

## External ecosystem tools

- bodsdata → https://github.com/openownership/bodsdata  
- RDF vocabulary → https://github.com/openownership/bodsld  

---

## 💡 AI & skills

- https://github.com/StephenAbbott/beneficial-ownership-data  
- https://github.com/StephenAbbott/bods-skill  

---

# 🔄 Key workflows

## Validate
BODS → Validator → Clean dataset  

## Convert
- Graph → Neo4j  
- Sanctions → FollowTheMoney  
- Analytics → GQL / BigQuery  
- Tabular → bodsdata  
- Linked data → RDF  

## Analyse
- Ownership chains  
- Control structures  
- Network risks  

## Integrate
- Procurement systems  
- Registries  
- AML pipelines  
- Knowledge graphs  

---

# 🌐 Why this matters

Transforming BODS into graph, tabular, and linked data formats enables:

- AI applications  
- Cross-dataset linking  
- Scalable risk detection  
- Real-world operational use  

---

# 📚 Resources

- https://standard.openownership.org/  
- https://www.openownership.org/  

---

# 🤝 Contributing

Contributions welcome:
- Data mappings  
- Conversion tools  
- Documentation  
- Example datasets  

---

# 🧩 Positioning

This is not a single tool.

It is a **modular interoperability layer for beneficial ownership data**.
