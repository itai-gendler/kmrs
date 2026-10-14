---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Visitor chooses Continue with the identity provider and signs in there",
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
      "text": "The provider returns a verified email that matches a User, ignoring case",
      "kind": "condition",
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
          "place": "web::public::sign-in"
        }
      }
    },
    {
      "text": "The Product signs that User in and opens the dashboard",
      "kind": "product",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": []
        }
      ],
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

# Sign in through an identity provider

## Trigger

A Visitor chooses Continue with a configured identity provider.

## Outcome

The person is signed in as the User whose email the provider confirmed.
