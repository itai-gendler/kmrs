---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin turns off Manual ordering for the Collection",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "collection",
          "effect": "reads",
          "facts": [
            "Manual ordering"
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
      "text": "The Product stops keeping a stored order for the Collection",
      "kind": "product",
      "entities": [
        {
          "entity": "collection",
          "effect": "changes",
          "facts": [
            "Manual ordering"
          ]
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

# Turn off manual ordering of a collection

## Trigger

An Admin turns off Manual ordering while editing a collection.

## Outcome

The collection lists its series by title by default.
