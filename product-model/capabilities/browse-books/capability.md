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
      "target": "webui/src/routes/library/books.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/routes/browse/books.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/books.rs#get_books"
    }
  ]
}
---

# Browse books

A User browses the books of one library or all libraries, filtered and sorted.
