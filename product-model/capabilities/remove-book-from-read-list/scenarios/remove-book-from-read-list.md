---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin chooses Remove for Books of the Read list",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "read-list",
          "effect": "reads",
          "facts": [
            "Books"
          ]
        },
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
          "place": "web::library::read-list"
        }
      }
    },
    {
      "text": "The Product takes the Books out of the Read list",
      "kind": "product",
      "entities": [
        {
          "entity": "read-list",
          "effect": "changes",
          "facts": [
            "Books"
          ]
        },
        {
          "entity": "book",
          "effect": "reads",
          "facts": []
        }
      ],
      "actor": "admin",
      "contexts": {
        "web": {
          "place": "web::library::read-list"
        }
      }
    }
  ]
}
---

# Remove books from a read list

## Trigger

An Admin removes books from a read list.

## Outcome

The read list no longer holds them.

## Edge cases

- Removing every book is refused; the Admin is told to delete the read list instead.
