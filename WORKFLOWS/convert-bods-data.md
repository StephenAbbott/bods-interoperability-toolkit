# Convert BODS Data

## When to use this

- To integrate BODS with systems that don't speak JSON-BODS natively
- To enable analysis that isn't practical on raw BODS statements (graph traversal, sanctions matching, SQL analytics)

## Conversion paths

| Target | Use for | Tool |
|---|---|---|
| **Neo4j** | Graph traversal, ownership chain queries, control path analysis | `bods-neo4j` mapping |
| **FollowTheMoney** | Sanctions and PEP linking, OpenSanctions integration | [bods-ftm](https://github.com/StephenAbbott/bods-ftm) |
| **GQL / BigQuery** | Large-scale SQL analytics | [bods-gql](https://github.com/StephenAbbott/bods-gql) |
| **Tabular (CSV / Parquet)** | Spreadsheet analysis, Pandas, downstream ETL | [bodsdata](https://github.com/openownership/bodsdata) |
| **RDF / Linked Data** | Knowledge graphs, SPARQL, semantic linking | [bodsld](https://github.com/openownership/bodsld) |
| **XML** | Legacy registry exchange formats | [bods-xml](https://github.com/StephenAbbott/bods-xml) |

## Outcome

BODS transformed into the operational format your target system expects, while preserving the underlying provenance and record structure.

## See also

- [Choose your tool](../DECISION-TREES/choose-your-tool.md)
- [Analyse ownership networks](analyse-ownership-networks.md)
