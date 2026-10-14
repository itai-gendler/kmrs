---
{
  "entities": [
    {
      "entity": "server-settings",
      "shows": [
        "Delete empty collections",
        "Delete empty read lists",
        "Remember me duration",
        "Thumbnail size",
        "Task pool size",
        "Server port",
        "Context path",
        "Kobo proxy",
        "Kobo port",
        "Kepubify path",
        "Max upload size"
      ],
      "collects": [
        "Delete empty collections",
        "Delete empty read lists",
        "Remember me duration",
        "Thumbnail size",
        "Task pool size",
        "Server port",
        "Context path",
        "Kobo proxy",
        "Kobo port",
        "Kepubify path",
        "Max upload size"
      ]
    }
  ],
  "entryPoints": [
    {
      "web": "/admin/settings"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/routes/admin/settings.tsx"
    }
  ]
}
---

# Settings

Server-wide options stored in the database.
