---
{
  "availability": [
    {
      "place": "kobo-sync"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/kobo.rs#sync_library"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/service/sync_point.rs#create_sync_point"
    }
  ]
}
---

# Sync Kobo library

A User's Kobo e-reader, pointed at the server with one of their API keys, receives the EPUB books they may access, their read lists as collections, and On Deck; each sync sends only what changed since the last one.
