---
{
  "entities": [
    {
      "entity": "smart-list",
      "shows": [
        "Name",
        "Summary",
        "Target",
        "Filters",
        "Visibility",
        "Shared with"
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
      "entity": "book",
      "shows": [
        "Title"
      ]
    },
    {
      "entity": "series",
      "shows": [
        "Title"
      ]
    },
    {
      "entity": "user",
      "shows": [
        "Email"
      ]
    }
  ],
  "entryPoints": [
    {
      "web": "/smart-lists/{smartListId}"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/routes/detail/smartlist.tsx"
    }
  ]
}
---

# Smart list

One smart list and what it matches right now.
