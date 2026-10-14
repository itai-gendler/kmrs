---
{
  "kind": "validation",
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
      "text": "The provider gave no email, an unverified email, or an email no User has while account creation is off",
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
      "text": "The Product returns the Visitor to the sign-in page with the reason",
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

# Identity provider sign-in is refused

## Trigger

A Visitor comes back from an identity provider that did not confirm a usable email, or whose email matches no account while account creation is off.

## Outcome

The person is back on the sign-in page with the reason the sign-in failed.
