---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin drags the Books of a manually ordered Read list into a new order and saves",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "read-list",
          "effect": "reads",
          "facts": [
            "Manual ordering",
            "Books"
          ]
        },
        {
          "entity": "book",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::library::read-list"
        }
      }
    },
    {
      "text": "The Product saves the new reading order",
      "kind": "product",
      "entities": [
        {
          "entity": "read-list",
          "effect": "changes",
          "facts": [
            "Books"
          ]
        },
        {
          "entity": "book",
          "effect": "reads",
          "facts": []
        }
      ],
      "actor": "admin",
      "contexts": {
        "web": {
          "place": "web::library::read-list"
        }
      }
    }
  ]
}
---

# Reorder a read list's books

## Trigger

An Admin drags books of a manually ordered read list.

## Outcome

The read list is read in the new order.
