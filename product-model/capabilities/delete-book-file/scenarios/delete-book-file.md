---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin chooses Delete file on a Book and confirms",
      "kind": "actor",
      "actor": "admin",
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
      "text": "The Product deletes the Book's file from disk and makes the Book Unavailable",
      "kind": "product",
      "entities": [
        {
          "entity": "book",
          "effect": "changes",
          "facts": [],
          "from": "Available",
          "to": "Unavailable"
        }
      ],
      "actor": "admin",
      "contexts": {
        "web": {
          "place": "web::library::book"
        }
      }
    }
  ]
}
---

# Delete a book's file

## Trigger

An Admin chooses Delete file on a book and confirms.

## Outcome

The file is gone from disk and the book is Unavailable.

## Edge cases

- A file that is missing or not writable is left alone.
- A folder left empty is deleted too.
