# Analyse Ownership Networks

## When to use this

- Investigations into corporate structures
- Risk detection across ownership chains
- Tracing ultimate beneficial owners through layered entities

## Workflow

```
BODS statements → Graph representation → Graph queries
```

Each entity statement becomes a node, each person statement becomes a node, and each relationship statement becomes an edge carrying the interest type, share percentage, and `directOrIndirect` flag.

## Example questions

- Who ultimately controls a given entity?
- What are the indirect ownership chains between a person and an entity?
- Are there circular ownership structures?
- Which entities share beneficial owners?
- Where do ownership chains cross jurisdictions?

## Tools

- **Neo4j** — property graph with Cypher queries
- **FollowTheMoney** — entity-centric graph used by OCCRP / OpenSanctions
- **RDF stores** — SPARQL queries for linked data contexts

## See also

- [Convert BODS data](convert-bods-data.md) — to get your BODS into a graph in the first place
- [Integrate with external systems](integrate-with-external-systems.md)
