---
{
  "entities": [
    {
      "entity": "api-key",
      "shows": [
        "Comment",
        "Created",
        "Last used"
      ],
      "collects": [
        "Comment"
      ]
    }
  ],
  "entryPoints": [
    {
      "web": "/account/api-keys"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/routes/account/api-keys.tsx"
    }
  ]
}
---

# API keys

The person's keys for third-party clients and sync.
