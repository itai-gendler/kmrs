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
  "domain": "libraries",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/libraries.rs#library_empty_trash"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/service/library_content.rs#empty_trash"
    }
  ]
}
---

# Empty trash

Unavailable series and books of a library are removed for good. It runs on request, or after every scan of a library with Empty trash after scan.
