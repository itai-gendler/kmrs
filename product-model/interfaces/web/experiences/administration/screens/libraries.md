---
{
  "entities": [
    {
      "entity": "library",
      "shows": [
        "Name",
        "Root folder",
        "Oneshots directory",
        "Scan interval",
        "Scan on startup",
        "Scanned file types",
        "Directory exclusions",
        "Import sources",
        "Series cover",
        "Analysis options",
        "Empty trash after scan"
      ],
      "collects": [
        "Name",
        "Root folder",
        "Oneshots directory",
        "Scan interval",
        "Scan on startup",
        "Scanned file types",
        "Directory exclusions",
        "Import sources",
        "Series cover",
        "Analysis options",
        "Empty trash after scan"
      ]
    }
  ],
  "entryPoints": [
    {
      "web": "/admin/libraries"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/routes/admin/libraries.tsx"
    }
  ]
}
---

# Libraries

Every library with its state, statistics, settings and actions.
