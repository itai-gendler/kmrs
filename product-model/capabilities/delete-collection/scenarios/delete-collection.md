---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin chooses Delete on the Collection and confirms",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "collection",
          "effect": "reads",
          "facts": [
            "Name"
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
      "text": "The Product deletes the Collection",
      "kind": "product",
      "entities": [
        {
          "entity": "collection",
          "effect": "removes"
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

# Delete a collection

## Trigger

An Admin chooses Delete on a collection and confirms.

## Outcome

The collection is gone; its series are untouched.
