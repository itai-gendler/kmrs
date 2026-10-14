---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin ticks a Library in the User's library access and saves",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Email",
            "Shared libraries"
          ]
        },
        {
          "entity": "library",
          "effect": "reads",
          "facts": [
            "Name"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::users"
        }
      }
    },
    {
      "text": "The Product shares the Library with the User and signs them out of every session",
      "kind": "product",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Shared libraries"
          ]
        },
        {
          "entity": "library",
          "effect": "reads",
          "facts": []
        }
      ],
      "actor": "admin",
      "contexts": {
        "web": {
          "place": "web::administration::users"
        }
      }
    }
  ]
}
---

# Share a library with a user

## Trigger

An Admin edits a user's library access and ticks a library.

## Outcome

The user sees that library's series and books and is signed out of every session.
