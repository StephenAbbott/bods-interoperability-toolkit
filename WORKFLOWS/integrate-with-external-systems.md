# Integrate BODS into Systems

## Use cases

- Procurement platforms (supplier due diligence)
- Corporate registries (publishing and consuming UBO data)
- AML and sanctions monitoring systems
- Data journalism and investigative pipelines

## Approach

1. **Validate** — confirm the BODS data is well-formed before anything else
2. **Convert** — transform BODS into the format the target system expects
3. **Integrate** — load into the pipeline, with a refresh strategy for new statements

## Considerations

- **Append-only semantics.** BODS is immutable: updates are new statements with the same `recordId` and `recordStatus: "updated"`. Your integration layer needs to decide whether to surface only the latest version of each record or to retain history.
- **Identity resolution.** BODS identifiers (`scheme` + `id`) help link entities across datasets, but you'll often need additional matching for persons.
- **Provenance.** Every statement carries a `source`. Preserve it — downstream users need to know where a claim came from.

## Outcome

BODS becomes part of your operational systems, not just a publication artifact.

## See also

- [Validate BODS data](validate-bods-data.md)
- [Convert BODS data](convert-bods-data.md)
