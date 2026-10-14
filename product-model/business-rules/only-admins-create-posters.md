---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "poster",
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
      "target": "crates/komga-server/src/api/series.rs#add_user_uploaded_series_thumbnail"
    }
  ]
}
---

# Only admins create posters

Posters of series, books, collections and read lists are managed by Admins.
