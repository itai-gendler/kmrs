---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin drags the Series of a manually ordered Collection into a new order and saves",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "collection",
          "effect": "reads",
          "facts": [
            "Manual ordering",
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
      "text": "The Product saves the new order of the Collection's Series",
      "kind": "product",
      "entities": [
        {
          "entity": "collection",
          "effect": "changes",
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
    }
  ]
}
---

# Reorder a collection's series

## Trigger

An Admin drags series of a manually ordered collection.

## Outcome

The collection lists its series in the new order.
