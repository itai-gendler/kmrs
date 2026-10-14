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
      "target": "crates/komga-server/src/api/books.rs#update_book_metadata"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/books.rs#update_book_metadata_by_batch"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/metadata/EditBooksDialog.tsx"
    }
  ]
}
---

# Edit book metadata

An Admin edits the metadata of one or several books. Every edited field is locked so refreshes keep it.
