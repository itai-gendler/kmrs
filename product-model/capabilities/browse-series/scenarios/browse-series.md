---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User opens Series and sets filters, sort or a first letter",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "series",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::library::library"
        }
      }
    },
    {
      "text": "The Product lists the Series the User may see",
      "kind": "product",
      "entities": [
        {
          "entity": "series",
          "effect": "reads",
          "facts": [
            "Title",
            "Status",
            "Book count"
          ]
        }
      ],
      "actor": "user",
      "contexts": {
        "web": {
          "place": "web::library::library"
        }
      }
    },
    {
      "text": "The User reads the Series with their read and unread counts",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "series",
          "effect": "reads",
          "facts": [
            "Title",
            "Status",
            "Book count"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::library::library"
        }
      }
    }
  ]
}
---

# Browse series

## Trigger

A User opens Series for a library or for all libraries.

## Outcome

The User sees the series they may access, with filters and sorting applied.
