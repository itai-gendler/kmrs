---
{
  "kind": "primary",
  "routes": {
    "kobo": "Kobo e-reader"
  },
  "steps": [
    {
      "text": "The User's Kobo e-reader asks for a sync with an API key in its address",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "api-key",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "kobo": {
          "place": "kobo-sync"
        }
      }
    },
    {
      "text": "The Product sends the Books, Read lists and Read progress added, changed or removed since the last sync of that API key",
      "kind": "product",
      "entities": [
        {
          "entity": "book",
          "effect": "reads",
          "facts": [
            "Title",
            "Authors",
            "Summary",
            "File size"
          ]
        },
        {
          "entity": "read-list",
          "effect": "reads",
          "facts": [
            "Name",
            "Books"
          ]
        },
        {
          "entity": "read-progress",
          "effect": "reads",
          "facts": [
            "Position"
          ]
        },
        {
          "entity": "api-key",
          "effect": "reads",
          "facts": []
        }
      ],
      "actor": "user",
      "contexts": {
        "kobo": {
          "place": "kobo-sync"
        }
      }
    },
    {
      "text": "The Product remembers what the API key's devices now have",
      "kind": "product",
      "entities": [
        {
          "entity": "api-key",
          "effect": "changes",
          "facts": [
            "Kobo sync point"
          ]
        }
      ],
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

# Sync a Kobo e-reader

## Trigger

The User's Kobo e-reader syncs.

## Outcome

The e-reader has every ready EPUB book the User may access, their read lists, and the current reading states.

## Edge cases

- What the server does not hold is answered by the Kobo store when Kobo proxy is on.
