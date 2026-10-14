---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User opens Smart lists",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "smart-list",
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
      "text": "The Product lists the Smart lists the User owns, public ones and ones shared with them",
      "kind": "product",
      "entities": [
        {
          "entity": "smart-list",
          "effect": "reads",
          "facts": [
            "Name",
            "Target",
            "Visibility"
          ]
        }
      ],
      "actor": "user",
      "contexts": {
        "web": {
          "place": "web::library::smart-lists"
        }
      }
    },
    {
      "text": "The User reads the Smart lists",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "smart-list",
          "effect": "reads",
          "facts": [
            "Name",
            "Target",
            "Visibility"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::library::smart-lists"
        }
      }
    }
  ]
}
---

# Browse smart lists

## Trigger

A User opens Smart lists.

## Outcome

The User sees their own lists, public lists and lists shared with them.
