---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "collection",
      "effect": "removes"
    }
  ],
  "permits": [
    {
      "actors": [
        "admin"
      ]
    },
    {
      "unattended": true
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

# Only admins delete collections

Collections are curated by Admins; users only browse them. Empty ones may also be removed by the server.
