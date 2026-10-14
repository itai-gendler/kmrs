---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User opens a Smart list",
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
      "text": "The Product evaluates the Smart list's filters over the Books or Series the User may see",
      "kind": "product",
      "entities": [
        {
          "entity": "book",
          "effect": "reads",
          "facts": [
            "Title"
          ]
        },
        {
          "entity": "series",
          "effect": "reads",
          "facts": [
            "Title"
          ]
        },
        {
          "entity": "smart-list",
          "effect": "reads",
          "facts": []
        }
      ],
      "actor": "user",
      "contexts": {
        "web": {
          "place": "web::library::smart-list"
        }
      }
    },
    {
      "text": "The User reads the matching Books or Series",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "book",
          "effect": "reads",
          "facts": [
            "Title"
          ]
        },
        {
          "entity": "series",
          "effect": "reads",
          "facts": [
            "Title"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::library::smart-list"
        }
      }
    }
  ]
}
---

# View a smart list

## Trigger

A User opens a smart list they may see.

## Outcome

The User sees what the list's filters match among the content they may see.
