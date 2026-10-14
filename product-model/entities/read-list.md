---
{
  "domain": "read-lists",
  "relations": [
    {
      "entity": "book",
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
      "target": "crates/komga-core/src/model/readlist.rs#ReadList"
    }
  ]
}
---

# Read list

A named reading order of books that admins curate across series and libraries.

## Information kept

- **Name** — unique among read lists
- **Summary** — description
- **Manual ordering** — whether its books keep the order they were put in
- **Books** — the books it holds, at least one
