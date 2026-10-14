---
{
  "entities": [
    {
      "entity": "read-list",
      "shows": [
        "Name",
        "Manual ordering",
        "Summary",
        "Books"
      ],
      "collects": [
        "Name",
        "Summary",
        "Books"
      ]
    },
    {
      "entity": "book",
      "shows": [
        "Title",
        "Number"
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
      "web": "/readlists/{readListId}"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/routes/detail/readlist.tsx"
    }
  ]
}
---

# Read list

One read list and its books.
