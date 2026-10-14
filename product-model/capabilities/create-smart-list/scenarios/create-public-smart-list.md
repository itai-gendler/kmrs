---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin enters a name, chooses a target, sets filters and picks Public or Shared with chosen users",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::library::smart-lists"
        }
      }
    },
    {
      "text": "The Product creates the Smart list owned by the Admin with that visibility",
      "kind": "product",
      "entities": [
        {
          "entity": "smart-list",
          "effect": "creates",
          "facts": [
            "Name",
            "Summary",
            "Target",
            "Filters",
            "Visibility",
            "Shared with"
          ]
        }
      ],
      "actor": "admin",
      "contexts": {
        "web": {
          "place": "web::library::smart-lists"
        }
      }
    }
  ]
}
---

# Create a smart list for others

## Trigger

An Admin creates a smart list and sets its visibility.

## Outcome

The Admin owns a list that is public or shared with chosen people.
