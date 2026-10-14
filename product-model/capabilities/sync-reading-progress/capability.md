---
{
  "availability": [
    {
      "place": "kobo-sync"
    },
    {
      "place": "koreader-sync"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/kobo.rs#update_state"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/koreader.rs#update_progress"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/koreader.rs#get_progress"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/koreader.rs#book_by_hash"
    }
  ]
}
---

# Sync reading progress

A Kobo e-reader or KOReader reports where the User is in a book, and the server's progress follows; KOReader can also fetch the server's progress.
