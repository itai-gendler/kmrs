---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User chooses Mark as read on a Book they are reading",
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
      "text": "The Product moves the User's Read progress to Completed at the last page",
      "kind": "product",
      "entities": [
        {
          "entity": "read-progress",
          "effect": "changes",
          "facts": [
            "Page",
            "Read date"
          ],
          "from": "In progress",
          "to": "Completed"
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

# Mark a book in progress as read

## Trigger

A User chooses Mark as read on a book they are reading.

## Outcome

The book is Completed for that User.
