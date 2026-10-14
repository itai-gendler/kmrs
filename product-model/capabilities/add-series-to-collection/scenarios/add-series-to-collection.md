---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin picks Series and the Collection to add them to",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "collection",
          "effect": "reads",
          "facts": [
            "Name"
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
      "text": "The Product appends the Series to the Collection",
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

# Add series to a collection

## Trigger

An Admin chooses Add to collection on selected series and picks a collection, or Add series on a collection.

## Outcome

The collection also holds those series.
