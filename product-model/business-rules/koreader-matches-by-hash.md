---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "sync-reading-progress"
    },
    {
      "type": "context",
      "context": {
        "place": "koreader-sync"
      }
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/koreader.rs#book_by_hash"
    }
  ]
}
---

# KOReader progress matches books by their KOReader hash

KOReader identifies a document by a partial hash of its file. A book has that hash only in libraries with Hash Koreader position on, and progress for a hash shared by several books is refused.
