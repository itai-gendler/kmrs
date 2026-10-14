---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin changes the Read list's name and summary and saves",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "read-list",
          "effect": "reads",
          "facts": [
            "Name",
            "Summary"
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
      "text": "The Product saves the Read list's name and summary",
      "kind": "product",
      "entities": [
        {
          "entity": "read-list",
          "effect": "changes",
          "facts": [
            "Name",
            "Summary"
          ]
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

# Edit a read list

## Trigger

An Admin chooses Edit details on a read list.

## Outcome

The read list has its new name and summary.

## Edge cases

- A name another read list already has is refused.
