---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin ticks Users under Shared with and saves",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "smart-list",
          "effect": "reads",
          "facts": [
            "Shared with"
          ]
        },
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Email"
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
      "text": "The Product shares the Smart list with those Users",
      "kind": "product",
      "entities": [
        {
          "entity": "smart-list",
          "effect": "changes",
          "facts": [
            "Shared with"
          ]
        },
        {
          "entity": "user",
          "effect": "reads",
          "facts": []
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

# Share a smart list with users

## Trigger

An Admin ticks users under Shared with.

## Outcome

Those users see the list.

## Edge cases

- A user that does not exist is refused.
