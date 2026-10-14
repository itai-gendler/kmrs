---
{
  "entities": [
    {
      "entity": "collection",
      "shows": [
        "Name",
        "Manual ordering",
        "Series"
      ],
      "collects": [
        "Name",
        "Series"
      ]
    },
    {
      "entity": "series",
      "shows": [
        "Title"
      ]
    }
  ],
  "entryPoints": [
    {
      "web": "/collections/{collectionId}"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/routes/detail/collection.tsx"
    }
  ]
}
---

# Collection

One collection and its series.
