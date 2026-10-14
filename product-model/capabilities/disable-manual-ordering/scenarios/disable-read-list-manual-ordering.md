---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin turns off Manual ordering for the Read list",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "read-list",
          "effect": "reads",
          "facts": [
            "Manual ordering"
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
      "text": "The Product stops keeping a stored order for the Read list",
      "kind": "product",
      "entities": [
        {
          "entity": "read-list",
          "effect": "changes",
          "facts": [
            "Manual ordering"
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

# Turn off manual ordering of a read list

## Trigger

An Admin turns off Manual ordering while editing a read list.

## Outcome

The read list lists its books by release date by default.
