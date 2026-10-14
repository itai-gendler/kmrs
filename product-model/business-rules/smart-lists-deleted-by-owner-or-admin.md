---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "smart-list",
      "effect": "removes"
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
      "target": "crates/komga-server/src/api/smartlists.rs#delete_smart_list_by_id"
    }
  ]
}
---

# A smart list is deleted by its owner or an admin

Its owner, or an Admin, deletes a smart list.
