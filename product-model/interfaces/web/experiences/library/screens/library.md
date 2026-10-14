---
{
  "entities": [
    {
      "entity": "series",
      "shows": [
        "Title",
        "Status",
        "Book count"
      ]
    },
    {
      "entity": "book",
      "shows": [
        "Title",
        "Number",
        "Media status"
      ]
    },
    {
      "entity": "read-progress",
      "shows": [
        "Page"
      ]
    },
    {
      "entity": "collection",
      "shows": [
        "Name",
        "Series"
      ],
      "collects": [
        "Name"
      ]
    },
    {
      "entity": "read-list",
      "shows": [
        "Name",
        "Books"
      ],
      "collects": [
        "Name"
      ]
    }
  ],
  "entryPoints": [
    {
      "web": "/series"
    },
    {
      "web": "/libraries/{libraryId}/series"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/browse/BrowseTabs.tsx"
    }
  ]
}
---

# Library

The series, books, collections and read lists of one library or of all libraries, with filters and selection.
