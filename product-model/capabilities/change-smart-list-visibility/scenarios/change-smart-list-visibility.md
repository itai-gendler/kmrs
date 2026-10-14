---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin picks Private, Public or Shared for the Smart list and saves",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "smart-list",
          "effect": "reads",
          "facts": [
            "Visibility"
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
      "text": "The Product saves the Smart list's visibility",
      "kind": "product",
      "entities": [
        {
          "entity": "smart-list",
          "effect": "changes",
          "facts": [
            "Visibility"
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

# Change a smart list's visibility

## Trigger

An Admin edits a smart list and picks Private, Public or Shared.

## Outcome

Only the owner and admins, every user, or the chosen users see the list.

## Edge cases

- Shared needs at least one chosen user.
