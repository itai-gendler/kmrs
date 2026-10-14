---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin chooses Delete on the Read list and confirms",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "read-list",
          "effect": "reads",
          "facts": [
            "Name"
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
      "text": "The Product deletes the Read list",
      "kind": "product",
      "entities": [
        {
          "entity": "read-list",
          "effect": "removes"
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

# Delete a read list

## Trigger

An Admin chooses Delete on a read list and confirms.

## Outcome

The read list is gone; its books are untouched.
