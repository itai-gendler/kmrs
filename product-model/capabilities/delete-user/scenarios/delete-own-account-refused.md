---
{
  "kind": "validation",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin tries to delete their own User account",
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
      "text": "The User to delete is the signed-in Admin",
      "kind": "condition",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": []
        },
        {
          "entity": "admin",
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
      "text": "The Product refuses the deletion",
      "kind": "product",
      "entities": [],
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

# Delete one's own account

## Trigger

An Admin tries to delete their own account on Users.

## Outcome

Nothing is deleted.
