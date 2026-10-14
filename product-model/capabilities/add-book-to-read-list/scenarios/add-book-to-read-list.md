---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin picks Books and the Read list to add them to",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "read-list",
          "effect": "reads",
          "facts": [
            "Name"
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
      "text": "The Product appends the Books to the Read list",
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

# Add books to a read list

## Trigger

An Admin chooses Add to read list on selected books and picks a read list, or Add books on a read list.

## Outcome

The read list also holds those books, after the ones it had.
