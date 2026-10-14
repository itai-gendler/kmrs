---
{
  "kind": "validation",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Visitor enters an email and a password",
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
      "text": "No User has that email with that password",
      "kind": "condition",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Email",
            "Password"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::sign-in"
        }
      }
    },
    {
      "text": "The Product refuses the sign-in with Invalid email or password",
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

# Sign in with a wrong email or password

## Trigger

A Visitor submits an email and password that do not match an account.

## Outcome

The person stays on the sign-in page with Invalid email or password.
