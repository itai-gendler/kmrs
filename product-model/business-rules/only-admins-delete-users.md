---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "user",
      "effect": "removes"
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
      "target": "crates/komga-server/src/api/users.rs#delete_user"
    }
  ]
}
---

# Only admins delete users

Deleting a user is an Admin's job, and never their own account.
