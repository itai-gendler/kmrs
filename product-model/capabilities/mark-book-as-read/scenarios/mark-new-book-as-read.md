---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User chooses Mark as read on a Book",
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
      "text": "The Product records the Book as Completed for the User at its last page",
      "kind": "product",
      "entities": [
        {
          "entity": "read-progress",
          "effect": "creates",
          "facts": [
            "Page",
            "Read date"
          ],
          "to": "Completed"
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

# Mark an unread book as read

## Trigger

A User chooses Mark as read on a book they have not started.

## Outcome

The book is Completed for that User.

## Edge cases

- Marking several selected books applies to each and reports how many failed.
