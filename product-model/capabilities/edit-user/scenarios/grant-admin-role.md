---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin turns on the Admin role for a User and saves",
      "kind": "actor",
      "actor": "admin",
      "entities": [
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
          "place": "web::administration::users"
        }
      }
    },
    {
      "text": "The Product gives the User the Admin role and signs them out of every session",
      "kind": "product",
      "entities": [
        {
          "entity": "admin",
          "effect": "creates",
          "facts": []
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
          "place": "web::administration::users"
        }
      }
    }
  ]
}
---

# Give a user the Admin role

## Trigger

An Admin edits a user and turns on the Admin role.

## Outcome

The user holds the Admin role and is signed out of every session.
