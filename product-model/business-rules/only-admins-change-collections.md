---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "collection",
      "effect": "changes"
    }
  ],
  "permits": [
    {
      "actors": [
        "admin"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/collections.rs"
    }
  ]
}
---

# Only admins change collections

Collections are curated by Admins; users only browse them.
