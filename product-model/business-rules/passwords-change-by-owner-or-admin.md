---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "user",
      "effect": "changes",
      "facts": [
        "Password"
      ]
    }
  ],
  "permits": [
    {
      "self": true
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
      "target": "crates/komga-server/src/api/users.rs#update_password_by_id"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/users.rs#update_my_password"
    }
  ]
}
---

# A password is changed by its owner or an admin

A User changes their own password; an Admin may set anyone's.
