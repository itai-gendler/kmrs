---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "admin",
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
      "target": "crates/komga-server/src/api/users.rs#update_user"
    }
  ]
}
---

# Only admins give the Admin role

The Admin role is given by another Admin; the first one comes with claiming the server.
