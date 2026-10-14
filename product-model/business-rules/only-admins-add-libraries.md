---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "library",
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
      "target": "crates/komga-server/src/api/libraries.rs#add_library"
    }
  ]
}
---

# Only admins add libraries

Adding a library is an Admin's job.
