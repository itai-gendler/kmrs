---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin chooses Delete for a User and confirms",
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
      "text": "The Product deletes the User with their reading progress, API keys and sessions",
      "kind": "product",
      "entities": [
        {
          "entity": "user",
          "effect": "removes"
        },
        {
          "entity": "api-key",
          "effect": "removes",
          "with": "user"
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

# Delete a user

## Trigger

An Admin chooses to delete a user and confirms.

## Outcome

The user, their reading progress, API keys, login activity and sessions are gone.
