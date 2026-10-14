---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "sync-kobo-library"
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
      "target": "crates/komga-server/src/service/sync_point.rs#create_sync_point"
    }
  ]
}
---

# Kobo e-readers receive only ready EPUB books

A Kobo sync includes the EPUB books the user may see whose analysis succeeded, plus the user's read lists as collections and an On Deck list.
