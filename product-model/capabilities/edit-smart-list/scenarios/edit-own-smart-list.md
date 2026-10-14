---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User changes the name, summary, target or filters of their Smart list and saves",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "smart-list",
          "effect": "reads",
          "facts": [
            "Name",
            "Summary",
            "Target",
            "Filters"
          ]
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
      "actor": "user",
      "contexts": {
        "web": {
          "place": "web::library::smart-list"
        }
      }
    }
  ]
}
---

# Edit one's own smart list

## Trigger

A User chooses Edit on a smart list they own.

## Outcome

The list matches with its new filters.
