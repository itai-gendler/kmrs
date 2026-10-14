---
{
  "kind": "primary",
  "routes": {
    "opds": "OPDS client"
  },
  "steps": [
    {
      "text": "The User downloads a Book from their OPDS catalog",
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
        "opds": {
          "place": "opds"
        }
      }
    },
    {
      "text": "The Product sends the Book's file",
      "kind": "product",
      "entities": [
        {
          "entity": "book",
          "effect": "reads",
          "facts": [
            "File"
          ]
        }
      ],
      "actor": "user",
      "contexts": {
        "opds": {
          "place": "opds"
        }
      }
    }
  ]
}
---

# Download a book in an OPDS client

## Trigger

A User's OPDS client follows a book's acquisition link.

## Outcome

The OPDS client has the book's file.
