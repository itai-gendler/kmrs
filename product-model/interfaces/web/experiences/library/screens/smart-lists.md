---
{
  "entities": [
    {
      "entity": "smart-list",
      "shows": [
        "Name",
        "Target",
        "Visibility"
      ],
      "collects": [
        "Name",
        "Summary",
        "Target",
        "Filters",
        "Visibility",
        "Shared with"
      ]
    },
    {
      "entity": "series",
      "shows": [
        "Title"
      ]
    },
    {
      "entity": "book",
      "shows": [
        "Title"
      ]
    }
  ],
  "entryPoints": [
    {
      "web": "/smart-lists"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/routes/browse/smartlists.tsx"
    }
  ]
}
---

# Smart lists

The smart lists the person may see.
