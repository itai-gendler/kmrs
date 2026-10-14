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
      "target": "crates/komga-server/src/api/books.rs#delete_book_file"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/service/book.rs#delete_book_files"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/browse/ConfirmDeleteFilesDialog.tsx"
    }
  ]
}
---

# Delete book file

An Admin deletes the files of one or several books from disk; the books become Unavailable until the trash is emptied.
