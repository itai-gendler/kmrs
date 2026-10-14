---
{
  "kind": "validation",
  "routes": {
    "kobo": "Kobo e-reader"
  },
  "steps": [
    {
      "text": "The User's Kobo e-reader asks for a sync",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "kobo": {
          "place": "kobo-sync"
        }
      }
    },
    {
      "text": "The User does not have Kobo sync",
      "kind": "condition",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Kobo sync"
          ]
        }
      ],
      "contexts": {
        "kobo": {
          "place": "kobo-sync"
        }
      }
    },
    {
      "text": "The Product refuses the sync",
      "kind": "product",
      "entities": [],
      "actor": "user",
      "contexts": {
        "kobo": {
          "place": "kobo-sync"
        }
      }
    }
  ]
}
---

# Sync a Kobo e-reader without Kobo sync

## Trigger

A Kobo e-reader syncs with the API key of a User without Kobo sync.

## Outcome

Nothing is sent.

## Edge cases

- An unknown API key is refused and recorded as a failed sign-in.
