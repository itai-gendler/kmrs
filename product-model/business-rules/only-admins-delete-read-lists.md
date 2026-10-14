---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "read-list",
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
      "target": "crates/komga-server/src/api/readlists.rs"
    }
  ]
}
---

# Only admins delete read lists

Read lists are curated by Admins; users only browse and read them. Empty ones may also be removed by the server.
