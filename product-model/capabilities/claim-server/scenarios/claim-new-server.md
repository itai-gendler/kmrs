---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The server has no account yet, so the sign-in page offers to claim it",
      "kind": "condition",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::public::sign-in"
        }
      }
    },
    {
      "text": "The Visitor enters an email and a password and chooses Create account",
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
      "text": "The Product creates the first User with every role and all libraries shared, holding the Admin role",
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
          "entity": "admin",
          "effect": "creates",
          "facts": [],
          "with": "user"
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
      "text": "The Product signs the new Admin in and opens the dashboard",
      "kind": "product",
      "entities": [
        {
          "entity": "admin",
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

# Claim a new server

## Trigger

A person opens the sign-in page of a server that has no account yet.

## Outcome

The server has its first account, an Admin holding every role with all libraries shared, and that person is signed in on the dashboard.

## Edge cases

- An email that is not well formed or a blank password is refused before anything is created.
