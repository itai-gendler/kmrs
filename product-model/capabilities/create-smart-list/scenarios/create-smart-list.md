---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User enters a name and summary, chooses Books or Series and sets filters",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "series",
          "effect": "reads",
          "facts": []
        },
        {
          "entity": "book",
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
      "text": "The Product creates a private Smart list owned by the User",
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
            "Visibility"
          ]
        },
        {
          "entity": "user",
          "effect": "reads",
          "facts": []
        }
      ],
      "actor": "user",
      "contexts": {
        "web": {
          "place": "web::library::smart-lists"
        }
      }
    }
  ]
}
---

# Create a smart list

## Trigger

A User chooses New smart list.

## Outcome

The User owns a private smart list with the chosen name, target and filters.
