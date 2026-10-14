---
{
  "kind": "validation",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User chooses Read on a Book",
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
      "text": "The User does not have Page streaming",
      "kind": "condition",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Page streaming"
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
      "text": "The Product refuses to serve the Book's pages",
      "kind": "product",
      "entities": [
        {
          "entity": "book",
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

# Read a book without Page streaming

## Trigger

A User without Page streaming opens a book to read it.

## Outcome

No page is served.
