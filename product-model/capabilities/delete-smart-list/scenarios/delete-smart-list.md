---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User chooses Delete on their Smart list and confirms",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "smart-list",
          "effect": "reads",
          "facts": [
            "Name"
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
      "text": "The Product deletes the Smart list",
      "kind": "product",
      "entities": [
        {
          "entity": "smart-list",
          "effect": "removes"
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

# Delete a smart list

## Trigger

A User chooses Delete on a smart list they own and confirms.

## Outcome

The list is gone for everyone who could see it.
