---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "smart-list",
      "effect": "changes",
      "facts": [
        "Visibility",
        "Shared with"
      ]
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
      "target": "crates/komga-server/src/api/smartlists.rs#update_smart_list_by_id"
    }
  ]
}
---

# Only admins set who sees a smart list

Visibility and the people a list is shared with are set by Admins; users' lists stay private.
