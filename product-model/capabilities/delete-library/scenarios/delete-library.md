---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin chooses Delete for a Library and confirms",
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
      "text": "The Product removes the Library with its Series and Books, leaving the files on disk",
      "kind": "product",
      "entities": [
        {
          "entity": "library",
          "effect": "removes",
          "from": "Available"
        },
        {
          "entity": "series",
          "effect": "removes",
          "from": "Available",
          "with": "library"
        },
        {
          "entity": "book",
          "effect": "removes",
          "from": "Available",
          "with": "library"
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

# Delete a library

## Trigger

An Admin chooses Delete library and confirms.

## Outcome

The library, its series and its books are gone from the server; the files stay where they were.
