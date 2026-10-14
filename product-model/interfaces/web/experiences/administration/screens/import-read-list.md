---
{
  "entities": [
    {
      "entity": "library",
      "shows": [
        "Name"
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
      "entity": "read-list",
      "shows": [
        "Name"
      ],
      "collects": [
        "Name"
      ]
    }
  ],
  "entryPoints": [
    {
      "web": "/import/readlist"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/routes/import/readlist.tsx"
    }
  ]
}
---

# Import read list

Matching a ComicRack .cbl file against the libraries.
