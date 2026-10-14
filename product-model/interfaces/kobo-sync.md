---
{
  "type": "api",
  "actors": [
    "user"
  ],
  "entryPoints": [
    {
      "api": "/kobo/{apiKey}/v1/library/sync"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/kobo.rs#router"
    }
  ]
}
---

# Kobo sync

The sync service a Kobo e-reader talks to once its store address is pointed at the server with one of the user's API keys.
