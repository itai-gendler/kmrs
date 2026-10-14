---
{
  "kind": "edge",
  "routes": {
    "kobo": "Kobo e-reader"
  },
  "steps": [
    {
      "text": "The User's Kobo e-reader reports its position in a Book",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "book",
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
      "text": "The User's Read progress on the Book is newer than the report",
      "kind": "condition",
      "entities": [
        {
          "entity": "read-progress",
          "effect": "reads",
          "facts": [
            "Read date"
          ]
        },
        {
          "entity": "book",
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
      "text": "The Product refuses the older progress",
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

# A device reports progress older than the server's

## Trigger

A Kobo e-reader reports a position older than the progress the server holds.

## Outcome

The newer progress is kept.
