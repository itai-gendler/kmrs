---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin selects Books, chooses Add to read list and types a New read list name",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "book",
          "effect": "reads",
          "facts": [
            "Title"
          ]
        },
        {
          "entity": "read-list",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::library::library"
        }
      }
    },
    {
      "text": "The Product creates the Read list holding the selected Books",
      "kind": "product",
      "entities": [
        {
          "entity": "read-list",
          "effect": "creates",
          "facts": [
            "Name",
            "Summary",
            "Manual ordering",
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
          "place": "web::library::library"
        }
      }
    }
  ]
}
---

# Create a read list from selected books

## Trigger

An Admin selects books, chooses Add to read list and enters a new name.

## Outcome

A new read list holds the selected books in that order.

## Edge cases

- A name another read list already has is refused.
