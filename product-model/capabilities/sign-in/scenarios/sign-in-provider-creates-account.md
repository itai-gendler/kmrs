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
      "text": "The provider's verified email matches no User and account creation is turned on",
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
      "text": "The Product creates a User for that email with File download and Page streaming and all libraries shared",
      "kind": "product",
      "entities": [
        {
          "entity": "user",
          "effect": "creates",
          "facts": [
            "Email",
            "Password",
            "File download",
            "Page streaming",
            "Kobo sync",
            "KOReader sync",
            "All libraries",
            "Shared libraries",
            "Age restriction",
            "Allowed labels",
            "Excluded labels"
          ]
        },
        {
          "entity": "library",
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
    },
    {
      "text": "The Product signs the new User in and opens the dashboard",
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

# First sign-in through an identity provider creates the account

## Trigger

A Visitor signs in through an identity provider with an email no account has, on a server whose operator turned on account creation.

## Outcome

A new User exists for that email, with File download and Page streaming and all libraries shared, and is signed in.
