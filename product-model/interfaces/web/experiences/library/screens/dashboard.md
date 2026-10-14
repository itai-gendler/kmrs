---
{
  "entities": [
    {
      "entity": "book",
      "shows": [
        "Title",
        "Number"
      ]
    },
    {
      "entity": "series",
      "shows": [
        "Title"
      ]
    },
    {
      "entity": "read-progress",
      "shows": [
        "Page"
      ]
    }
  ],
  "entryPoints": [
    {
      "web": "/dashboard"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/routes/dashboard.tsx"
    }
  ]
}
---

# Dashboard

What to read next, for all libraries or one library.
