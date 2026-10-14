---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin changes the filters of another user's Smart list and saves",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "smart-list",
          "effect": "reads",
          "facts": [
            "Name",
            "Target",
            "Filters"
          ]
        },
        {
          "entity": "user",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::library::smart-list"
        }
      }
    },
    {
      "text": "The Product saves the Smart list",
      "kind": "product",
      "entities": [
        {
          "entity": "smart-list",
          "effect": "changes",
          "facts": [
            "Name",
            "Summary",
            "Target",
            "Filters"
          ]
        }
      ],
      "actor": "admin",
      "contexts": {
        "web": {
          "place": "web::library::smart-list"
        }
      }
    }
  ]
}
---

# An Admin edits someone else's smart list

## Trigger

An Admin chooses Edit on a smart list another user owns.

## Outcome

The list matches with its new filters and keeps its owner.
