---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin chooses Analyze on a Series",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "series",
          "effect": "reads",
          "facts": [
            "Title"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::library::series"
        }
      }
    },
    {
      "text": "The Product queues analysis of each Book of the Series and records its format, pages and media status",
      "kind": "product",
      "entities": [
        {
          "entity": "book",
          "effect": "changes",
          "facts": [
            "Format",
            "Page count",
            "Media status"
          ]
        },
        {
          "entity": "series",
          "effect": "reads",
          "facts": []
        }
      ],
      "actor": "admin",
      "contexts": {
        "web": {
          "place": "web::library::series"
        }
      }
    }
  ]
}
---

# Analyze a series or a book

## Trigger

An Admin chooses Analyze on a series or a book.

## Outcome

The books have a fresh media status, format and page count.

## Edge cases

- A file that cannot be read gets the media status Error; an unsupported type gets Unsupported; a file changed on disk since its analysis is Outdated until analyzed again.
