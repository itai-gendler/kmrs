---
{
  "availability": [
    {
      "place": "web::library"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/routes/detail/series.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/routes/detail/oneshot.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/series.rs#get_series_by_id"
    }
  ]
}
---

# View series

A User opens a series, or a oneshot, to see its metadata, its books and how far they read.
