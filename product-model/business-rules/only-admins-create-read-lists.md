---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "read-list",
      "effect": "creates"
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
      "target": "crates/komga-server/src/api/readlists.rs"
    }
  ]
}
---

# Only admins create read lists

Read lists are curated by Admins; users only browse and read them.
