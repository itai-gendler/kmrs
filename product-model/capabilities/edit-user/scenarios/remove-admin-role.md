---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin turns off the Admin role for another User and saves",
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
      "text": "The Product takes the Admin role away and signs that User out of every session",
      "kind": "product",
      "entities": [
        {
          "entity": "admin",
          "effect": "removes"
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

# Take the Admin role from a user

## Trigger

An Admin edits another admin and turns off the Admin role.

## Outcome

That person is an ordinary user and is signed out of every session.
