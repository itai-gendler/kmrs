---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin turns on Share every library for the User and saves",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Email",
            "All libraries"
          ]
        },
        {
          "entity": "library",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::users"
        }
      }
    },
    {
      "text": "The Product shares every library with the User and signs them out of every session",
      "kind": "product",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "All libraries",
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

# Share every library with a user

## Trigger

An Admin turns on all libraries for a user.

## Outcome

The user reaches every library, including ones added later.
