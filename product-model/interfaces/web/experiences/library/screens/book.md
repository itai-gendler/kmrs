---
{
  "entities": [
    {
      "entity": "book",
      "shows": [
        "Title",
        "Number",
        "Summary",
        "Authors",
        "Release date",
        "Format",
        "Page count",
        "File name",
        "File size",
        "Media status",
        "Sort number",
        "Tags",
        "ISBN",
        "Links",
        "Locked fields"
      ],
      "collects": [
        "Title",
        "Number",
        "Sort number",
        "Summary",
        "Release date",
        "Authors",
        "Tags",
        "ISBN",
        "Links",
        "Locked fields"
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
      "web": "/book/{bookId}"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/routes/detail/book.tsx"
    }
  ]
}
---

# Book

One book: its metadata, file and progress.
