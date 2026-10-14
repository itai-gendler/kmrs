---
{
  "type": "web",
  "actors": [
    "visitor",
    "user",
    "admin"
  ],
  "entryPoints": [
    {
      "web": "/"
    }
  ],
  "languages": [
    "en",
    "de",
    "es",
    "fr",
    "it",
    "ja",
    "ko",
    "ru",
    "zh-Hans",
    "zh-Hant"
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/router.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/webui.rs"
    }
  ]
}
---

# Web UI

The kmweb web UI, embedded in the server and served at its root: reading, browsing, account settings and administration.
