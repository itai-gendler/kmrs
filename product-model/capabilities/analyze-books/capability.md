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
      "target": "crates/komga-server/src/api/libraries.rs#library_analyze"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/books.rs#book_analyze"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/series.rs#series_analyze"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/service/processor.rs"
    }
  ]
}
---

# Analyze

An Admin has books' files read again to find their format, pages and readability. New and changed books are analyzed after every scan as well.
