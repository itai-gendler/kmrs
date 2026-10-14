---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "series",
      "effect": "removes"
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
      "target": "crates/komga-server/src/service/library_content.rs#empty_trash"
    }
  ]
}
---

# Only admins and the server remove series for good

Series leave the server when an Admin empties the trash or deletes their library, or when the trash empties itself after a scan.
