---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "series",
      "effect": "changes",
      "facts": [
        "Title",
        "Sort title",
        "Status",
        "Summary",
        "Reading direction",
        "Publisher",
        "Age rating",
        "Language",
        "Genres",
        "Tags",
        "Total book count",
        "Sharing labels",
        "Links",
        "Alternate titles"
      ]
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
      "target": "crates/komga-server/src/api/series.rs#update_series_metadata"
    }
  ]
}
---

# Only admins and the server's refreshes change series metadata

Admins edit series metadata; scans and refreshes update it from the files.
