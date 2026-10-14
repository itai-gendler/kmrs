---
{
  "availability": [
    {
      "place": "web::administration"
    },
    {
      "place": "web::library"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/libraries.rs#library_refresh_metadata"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/series.rs#series_refresh_metadata"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/books.rs#book_refresh_metadata"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-media/src/metadata/patch.rs"
    }
  ]
}
---

# Refresh metadata

An Admin has series and book metadata read again from the library's import sources and local artwork. Locked fields keep their values.
