---
{
  "singleton": true,
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/settings.rs#get_server_settings"
    }
  ]
}
---

# Server settings

The server-wide options stored in the database.

## Information kept

- **Delete empty collections** — whether collections left without series are removed
- **Delete empty read lists** — whether read lists left without books are removed
- **Remember me duration** — how many days Keep me signed in lasts
- **Thumbnail size** — the size generated posters are made at
- **Task pool size** — how many background tasks run at once
- **Server port** — the port the server listens on
- **Context path** — the path the server is served under
- **Kobo proxy** — whether Kobo requests the server cannot answer go to the Kobo store
- **Kobo port** — the port given to Kobo e-readers
- **Kepubify path** — where the kepubify converter is
- **Max upload size** — the largest file that can be uploaded
