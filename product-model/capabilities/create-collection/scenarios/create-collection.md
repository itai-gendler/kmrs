---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin selects Series, chooses Add to collection and types a New collection name",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "series",
          "effect": "reads",
          "facts": [
            "Title"
          ]
        },
        {
          "entity": "collection",
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
      "text": "The Product creates the Collection holding the selected Series",
      "kind": "product",
      "entities": [
        {
          "entity": "collection",
          "effect": "creates",
          "facts": [
            "Name",
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
      "actor": "admin",
      "contexts": {
        "web": {
          "place": "web::library::library"
        }
      }
    }
  ]
}
---

# Create a collection from selected series

## Trigger

An Admin selects series, chooses Add to collection and enters a new name.

## Outcome

A new collection holds the selected series.
