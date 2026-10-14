---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin chooses Analyze for a Library",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "library",
          "effect": "reads",
          "facts": [
            "Name"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::libraries"
        }
      }
    },
    {
      "text": "The Product queues analysis of each Book in the Library and records its format, pages and media status",
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
          "entity": "library",
          "effect": "reads",
          "facts": []
        }
      ],
      "actor": "admin",
      "contexts": {
        "web": {
          "place": "web::administration::libraries"
        }
      }
    }
  ]
}
---

# Analyze a library

## Trigger

An Admin chooses Analyze in a library's actions.

## Outcome

Every book of the library has a fresh media status, format and page count.
