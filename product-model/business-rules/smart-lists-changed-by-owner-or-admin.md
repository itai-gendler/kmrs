---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "smart-list",
      "effect": "changes"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "owns",
          "entity": "user"
        }
      ]
    },
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
      "target": "crates/komga-server/src/api/smartlists.rs#require_owner_or_admin"
    }
  ]
}
---

# A smart list is changed by its owner or an admin

Its owner, or an Admin, edits a smart list.
