---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User chooses Download on a Book",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "book",
          "effect": "reads",
          "facts": [
            "Title",
            "File name"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::library::book"
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
        "web": {
          "place": "web::library::book"
        }
      }
    }
  ]
}
---

# Download a book

## Trigger

A User chooses Download on a book.

## Outcome

The User has the book's original file.
