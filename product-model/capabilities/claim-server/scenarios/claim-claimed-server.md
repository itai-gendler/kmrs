---
{
  "kind": "validation",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Visitor submits an email and a password to claim the server",
      "kind": "actor",
      "actor": "visitor",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::public::sign-in"
        }
      }
    },
    {
      "text": "The server already has at least one User",
      "kind": "condition",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::sign-in"
        }
      }
    },
    {
      "text": "The Product refuses the claim because the server has already been claimed",
      "kind": "product",
      "entities": [],
      "actor": "visitor",
      "contexts": {
        "web": {
          "place": "web::public::sign-in"
        }
      }
    }
  ]
}
---

# Claim a server that is already claimed

## Trigger

A claim request reaches a server that already has an account.

## Outcome

Nothing is created; the server answers that it has already been claimed.
