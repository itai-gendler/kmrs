---
{
  "availability": [
    {
      "place": "web::library"
    },
    {
      "place": "opds"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/routes/read.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/reader/epub/EpubReader.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/books.rs#get_book_page_by_number"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/books.rs#mark_read_progress"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/opds_v1.rs#get_book_page_opds"
    }
  ]
}
---

# Read book

A User reads a book page by page, or an EPUB in its own reader; progress is saved as they go. Peek reads without saving progress. OPDS clients stream pages the same way.
