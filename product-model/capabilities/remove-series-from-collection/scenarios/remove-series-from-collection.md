---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin chooses Remove for Series of the Collection",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "collection",
          "effect": "reads",
          "facts": [
            "Name",
            "Series"
          ]
        },
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
          "place": "web::library::collection"
        }
      }
    },
    {
      "text": "The Product takes the Series out of the Collection",
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

# Remove series from a collection

## Trigger

An Admin removes series from a collection.

## Outcome

The collection no longer holds them.
