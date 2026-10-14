---
{
  "kind": "primary",
  "routes": {
    "kobo": "Kobo e-reader"
  },
  "steps": [
    {
      "text": "The User's Kobo e-reader downloads a synced Book",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "book",
          "effect": "reads",
          "facts": [
            "Title"
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
      "text": "The Product sends the Book's file, converted to kepub when a Kepubify path is set",
      "kind": "product",
      "entities": [
        {
          "entity": "book",
          "effect": "reads",
          "facts": [
            "File"
          ]
        },
        {
          "entity": "server-settings",
          "effect": "reads",
          "facts": [
            "Kepubify path"
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

# Download a book to a Kobo e-reader

## Trigger

A Kobo e-reader downloads a book it received from a sync.

## Outcome

The e-reader has the book, converted to kepub when the server can convert it.
