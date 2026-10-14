---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User opens a Book",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "book",
          "effect": "reads",
          "facts": [
            "Title",
            "Number",
            "Summary",
            "Authors",
            "Release date",
            "Format",
            "Page count",
            "File name",
            "File size",
            "Media status"
          ]
        },
        {
          "entity": "read-progress",
          "effect": "reads",
          "facts": [
            "Page"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::library::book"
        }
      }
    }
  ]
}
---

# View a book

## Trigger

A User opens a book.

## Outcome

The User sees the book's metadata, format, pages, release date and progress.

## Edge cases

- A book whose analysis failed shows why it cannot be read.
