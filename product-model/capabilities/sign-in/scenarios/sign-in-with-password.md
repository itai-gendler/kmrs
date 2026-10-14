---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Visitor enters their email and password and chooses whether to stay signed in",
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
      "text": "The Product finds the User by email, ignoring case, and checks the password",
      "kind": "product",
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
      "actor": "visitor",
      "contexts": {
        "web": {
          "place": "web::public::sign-in"
        }
      }
    },
    {
      "text": "The Product signs the person in and opens the dashboard or the page they first asked for",
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

# Sign in with email and password

## Trigger

A Visitor opens the sign-in page of a claimed server.

## Outcome

The person is signed in and sees the dashboard or the page they first asked for.

## Edge cases

- With Keep me signed in, the browser stays signed in for the server's Remember me duration.
- When the operator hides the password form and exactly one identity provider is configured, the sign-in page sends the person straight to that provider.
