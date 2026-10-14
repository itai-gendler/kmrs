---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "login-activity",
      "effect": "reads"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "has",
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
      "target": "crates/komga-server/src/api/users.rs#authentication_activity"
    }
  ]
}
---

# Login activity is read by its user or an admin

A User reads the activity of their own account; an Admin reads everyone's.
