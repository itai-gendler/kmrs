---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "library",
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
      "target": "crates/komga-server/src/api/libraries.rs#delete_library_by_id"
    }
  ]
}
---

# Only admins delete libraries

Deleting a library is an Admin's job.
