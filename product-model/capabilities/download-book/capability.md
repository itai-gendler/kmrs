---
{
  "availability": [
    {
      "place": "web::library"
    },
    {
      "place": "opds"
    },
    {
      "place": "kobo-sync"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/books.rs#download_book_file_internal"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/kobo.rs#get_book_file"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/detail/DownloadLink.tsx"
    }
  ]
}
---

# Download book

A User with File download downloads a book's file, from the web UI, an OPDS client or a Kobo e-reader.
