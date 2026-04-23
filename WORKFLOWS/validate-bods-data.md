# Validate BODS Data

## When to use this

- Before publishing data
- Before converting BODS into another format
- When debugging data issues reported by downstream consumers

## Steps

1. Run a BODS validator against your dataset
2. Review reported schema and content errors
3. Fix structural issues and revalidate until the dataset is clean

## Common issues

- Missing required statements (e.g. a relationship statement referencing an entity statement that isn't in the dataset)
- Invalid ownership links (`subject` or `interestedParty` pointing to a non-existent `statementId`)
- Schema mismatch between v0.3 and v0.4 (e.g. using `ownershipOrControlStatement` under v0.4, or hyphenated interest type codes like `voting-rights` instead of camelCase `votingRights`)
- Missing `recordId` / `recordStatus` (required in v0.4)

## Output

A clean, valid BODS dataset ready for publication, conversion, or analysis.

## See also

- [Convert BODS data](convert-bods-data.md)
- [BODS changelog (v0.3 → v0.4)](https://standard.openownership.org/en/0.4.0/standard/changelog.html)
