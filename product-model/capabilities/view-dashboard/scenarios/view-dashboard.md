---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User opens the dashboard",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::library::dashboard"
        }
      }
    },
    {
      "text": "The Product lists Books with Read progress In progress, the next unread Book of each Series being read, and recent Series and Books",
      "kind": "product",
      "entities": [
        {
          "entity": "read-progress",
          "effect": "reads",
          "facts": [
            "Page",
            "Read date"
          ]
        },
        {
          "entity": "book",
          "effect": "reads",
          "facts": [
            "Title",
            "Number",
            "Release date",
            "Added"
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
      "actor": "user",
      "contexts": {
        "web": {
          "place": "web::library::dashboard"
        }
      }
    },
    {
      "text": "The User reads the Keep Reading, On Deck and recent rows",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "book",
          "effect": "reads",
          "facts": [
            "Title",
            "Number"
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
          "entity": "read-progress",
          "effect": "reads",
          "facts": [
            "Page"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::library::dashboard"
        }
      }
    }
  ]
}
---

# View the dashboard

## Trigger

A User opens the dashboard, for all libraries or one library.

## Outcome

The User sees books in progress, the next book of series they are reading, and what is new.

## Edge cases

- The All dashboard shows only pinned libraries when the User has pinned some.
- A server without content shows Nothing here yet.
