---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin enters a new password for the User",
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
      "text": "The Product replaces the User's password and signs them out of every session",
      "kind": "product",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Password"
          ]
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

# Set another user's password

## Trigger

An Admin chooses to change the password of a User on Users.

## Outcome

That user's password is the new one and all of their sessions are signed out.
