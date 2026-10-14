---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "admin",
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
      "target": "crates/komga-server/src/api/users.rs#update_user"
    }
  ]
}
---

# Only admins take the Admin role away

Taking the Admin role away is another Admin's job.
