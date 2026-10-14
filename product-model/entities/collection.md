---
{
  "domain": "collections",
  "relations": [
    {
      "entity": "series",
      "verb": "includes",
      "cardinality": "many-to-many"
    },
    {
      "entity": "poster",
      "verb": "has",
      "cardinality": "one-to-many"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-core/src/model/collection.rs#SeriesCollection"
    }
  ]
}
---

# Collection

A named group of series that admins curate across libraries.

## Information kept

- **Name** — unique among collections
- **Manual ordering** — whether its series keep the order they were put in
- **Series** — the series it holds, at least one
