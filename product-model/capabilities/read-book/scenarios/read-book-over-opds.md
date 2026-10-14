---
{
  "kind": "primary",
  "routes": {
    "opds": "OPDS client"
  },
  "steps": [
    {
      "text": "The User opens a Book in their OPDS reader",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "book",
          "effect": "reads",
          "facts": [
            "Title",
            "Page count"
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
      "text": "The Product serves the Book's pages one at a time",
      "kind": "product",
      "entities": [
        {
          "entity": "book",
          "effect": "reads",
          "facts": [
            "Page images"
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

# Stream a book's pages in an OPDS client

## Trigger

A User's OPDS reader opens a book from the catalog with page streaming.

## Outcome

The OPDS reader shows the book's pages one by one.
