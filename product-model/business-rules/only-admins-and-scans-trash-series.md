---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "series",
      "effect": "changes",
      "to": "Unavailable"
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
      "target": "crates/komga-server/src/service/series.rs#delete_series_files"
    }
  ]
}
---

# Only admins and scans make series Unavailable

A series becomes Unavailable when an Admin deletes its files or a scan finds its folder gone.
