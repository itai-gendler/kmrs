---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin unticks Users under Shared with and saves",
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
      "text": "The Product stops sharing the Smart list with those Users",
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

# Stop sharing a smart list with users

## Trigger

An Admin unticks users under Shared with.

## Outcome

Those users no longer see the list.

## Edge cases

- Unticking the last user of a Shared list is refused while it stays Shared.
