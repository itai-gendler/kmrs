---
{
  "kind": "validation",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User enters a name and filters",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::library::smart-lists"
        }
      }
    },
    {
      "text": "One of the User's Smart lists already has that name",
      "kind": "condition",
      "entities": [
        {
          "entity": "smart-list",
          "effect": "reads",
          "facts": [
            "Name"
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
          "place": "web::library::smart-lists"
        }
      }
    },
    {
      "text": "The Product refuses the new list",
      "kind": "product",
      "entities": [],
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

# Create a smart list with a name already used

## Trigger

A User names a new smart list like one of their own.

## Outcome

No list is created.
