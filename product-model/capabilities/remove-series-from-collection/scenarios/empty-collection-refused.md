---
{
  "kind": "validation",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin removes every Series from the Collection",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "collection",
          "effect": "reads",
          "facts": [
            "Series"
          ]
        },
        {
          "entity": "series",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::library::collection"
        }
      }
    },
    {
      "text": "No series would be left in the Collection",
      "kind": "condition",
      "entities": [
        {
          "entity": "collection",
          "effect": "reads",
          "facts": [
            "Series"
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
          "place": "web::library::collection"
        }
      }
    },
    {
      "text": "The Product refuses to empty the Collection",
      "kind": "product",
      "entities": [
        {
          "entity": "collection",
          "effect": "reads",
          "facts": []
        }
      ],
      "actor": "admin",
      "contexts": {
        "web": {
          "place": "web::library::collection"
        }
      }
    }
  ]
}
---

# Remove every series from a collection

## Trigger

An Admin tries to save a collection with no series left.

## Outcome

The collection keeps its series; the Admin is told to delete it instead.
