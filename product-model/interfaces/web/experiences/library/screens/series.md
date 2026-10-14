---
{
  "entities": [
    {
      "entity": "series",
      "shows": [
        "Title",
        "Status",
        "Summary",
        "Publisher",
        "Age rating",
        "Genres",
        "Tags",
        "Links",
        "Book count",
        "Sort title",
        "Reading direction",
        "Language",
        "Total book count",
        "Sharing labels",
        "Alternate titles",
        "Locked fields"
      ],
      "collects": [
        "Title",
        "Sort title",
        "Status",
        "Summary",
        "Reading direction",
        "Publisher",
        "Age rating",
        "Language",
        "Genres",
        "Tags",
        "Total book count",
        "Sharing labels",
        "Links",
        "Alternate titles",
        "Locked fields"
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
    },
    {
      "entity": "poster",
      "shows": [
        "Type",
        "Image"
      ],
      "collects": [
        "Image"
      ]
    }
  ],
  "entryPoints": [
    {
      "web": "/series/{seriesId}"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/routes/detail/series.tsx"
    }
  ]
}
---

# Series

One series or oneshot: its metadata, posters and books.
