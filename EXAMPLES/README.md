# Examples

## `minimal-bods-dataset.json`

A minimal valid BODS v0.4 dataset showing all three statement types:

- **Entity statement** — Acme Holdings Ltd, a UK registered company
- **Person statement** — Jane Smith, known person, British
- **Relationship statement** — Jane Smith holds 75% shareholding and 75% voting rights in Acme Holdings Ltd

The relationship statement links the person and entity by referencing their `statementId` values via `subject.describedByEntityStatement` and `interestedParty.describedByPersonStatement`.

Use this as a starting point for:

- Testing validators
- Prototyping conversions (Neo4j, FTM, RDF, tabular)
- Understanding the v0.4 record structure

## Notes on v0.4

- There is no top-level `statementType` field in v0.4. The type of a statement is determined by the structure of its `recordDetails`:
  - Entity statement → `recordDetails.entityType`
  - Person statement → `recordDetails.personType`
  - Relationship statement → `recordDetails.subject` + `recordDetails.interestedParty`
- `recordId` and `recordStatus` are how BODS tracks record lifecycle across immutable statements. To update a record, publish a new statement with the same `recordId` and `recordStatus: "updated"`.
- Interest type codes are camelCase (`votingRights`), not hyphenated (`voting-rights` was v0.3).
- `source.type` is a single string (e.g. `"officialRegister"`), not an array.
