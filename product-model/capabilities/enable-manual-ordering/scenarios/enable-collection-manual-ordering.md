---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin turns on Manual ordering for the Collection",
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
      "text": "The Product keeps the Collection's Series in their stored order",
      "kind": "product",
      "entities": [
        {
          "entity": "collection",
          "effect": "changes",
          "facts": [
            "Manual ordering"
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

# Turn on manual ordering of a collection

## Trigger

An Admin turns on Manual ordering while editing a collection.

## Outcome

The collection lists its series in the stored order by default.
