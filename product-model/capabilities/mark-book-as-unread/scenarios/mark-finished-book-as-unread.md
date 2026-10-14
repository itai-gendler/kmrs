---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User chooses Mark as unread on a Book",
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
      "text": "The Product deletes the User's Read progress on the Book",
      "kind": "product",
      "entities": [
        {
          "entity": "read-progress",
          "effect": "removes",
          "from": "Completed"
        },
        {
          "entity": "book",
          "effect": "reads",
          "facts": []
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

# Mark a read book as unread

## Trigger

A User chooses Mark as unread on a book they finished.

## Outcome

The book is unread for that User again.
