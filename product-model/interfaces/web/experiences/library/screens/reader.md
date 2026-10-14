---
{
  "entities": [
    {
      "entity": "book",
      "shows": [
        "Page images",
        "Page count"
      ]
    }
  ],
  "entryPoints": [
    {
      "web": "/book/{bookId}/read"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/routes/read.tsx"
    }
  ]
}
---

# Reader

Reading one book, page by page or as reflowed EPUB text.
