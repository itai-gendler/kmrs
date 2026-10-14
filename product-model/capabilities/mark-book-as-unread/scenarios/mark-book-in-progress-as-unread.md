---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User chooses Mark as unread on a Book they are reading",
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
          "from": "In progress"
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

# Mark a book in progress as unread

## Trigger

A User chooses Mark as unread on a book they are reading.

## Outcome

The book is unread for that User again.
