---
{
  "type": "api",
  "actors": [
    "user"
  ],
  "entryPoints": [
    {
      "api": "/koreader/syncs/progress"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/koreader.rs#router"
    }
  ]
}
---

# KOReader sync

A KOReader progress sync server; KOReader signs in with one of the user's API keys.
