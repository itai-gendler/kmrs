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
      "target": "webui/src/routes/library/series.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/routes/browse/series.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/series.rs#get_series"
    }
  ]
}
---

# Browse series

A User browses the series of one library or all libraries, filtered, sorted and jumped to by first letter.
