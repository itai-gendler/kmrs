---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "library",
      "effect": "changes"
    }
  ],
  "permits": [
    {
      "actors": [
        "admin"
      ]
    },
    {
      "unattended": true
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/libraries.rs#update_library_by_id"
    }
  ]
}
---

# Only admins and scans change libraries

An Admin changes a library's settings; the server's own scans mark it Available or Unavailable.
