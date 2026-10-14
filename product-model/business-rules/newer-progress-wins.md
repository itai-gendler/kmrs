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
        "place": "kobo-sync"
      }
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/books.rs#mark_progression"
    }
  ]
}
---

# Older progress never replaces newer progress

A device reporting a position older than the progress the server holds is refused.
