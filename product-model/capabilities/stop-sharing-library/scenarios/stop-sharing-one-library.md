---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin unticks a Library in the User's library access and saves",
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
      "text": "The Product stops sharing the Library with the User and signs them out of every session",
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

# Stop sharing a library with a user

## Trigger

An Admin unticks a library in a user's library access.

## Outcome

The user no longer sees that library's content and is signed out of every session.
