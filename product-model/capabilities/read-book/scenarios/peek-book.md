---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User chooses Peek on a Book",
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
        "web": {
          "place": "web::library::book"
        }
      }
    },
    {
      "text": "The User turns the pages of the Book",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "book",
          "effect": "reads",
          "facts": [
            "Page images",
            "Page count"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::library::reader"
        }
      }
    },
    {
      "text": "The Product leaves the User's Read progress as it was",
      "kind": "product",
      "entities": [
        {
          "entity": "read-progress",
          "effect": "reads",
          "facts": []
        }
      ],
      "actor": "user",
      "contexts": {
        "web": {
          "place": "web::library::reader"
        }
      }
    }
  ]
}
---

# Peek at a book

## Trigger

A User chooses Peek on a book.

## Outcome

The User reads the book and their progress is unchanged.
