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
      "target": "crates/komga-server/src/api/series.rs#delete_series_file"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/service/series.rs#delete_series_files"
    }
  ]
}
---

# Delete series files

An Admin deletes all files of one or several series from disk; the series and its books become Unavailable.
