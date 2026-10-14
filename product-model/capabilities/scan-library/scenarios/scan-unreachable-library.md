---
{
  "kind": "edge",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin chooses Scan for a Library",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "library",
          "effect": "reads",
          "facts": [
            "Name"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::libraries"
        }
      }
    },
    {
      "text": "The Library's root folder cannot be read",
      "kind": "condition",
      "entities": [
        {
          "entity": "library",
          "effect": "reads",
          "facts": [
            "Root folder"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::libraries"
        }
      }
    },
    {
      "text": "The Product marks the Library Unavailable and stops the scan",
      "kind": "product",
      "entities": [
        {
          "entity": "library",
          "effect": "changes",
          "facts": [],
          "from": "Available",
          "to": "Unavailable"
        }
      ],
      "actor": "admin",
      "contexts": {
        "web": {
          "place": "web::administration::libraries"
        }
      }
    }
  ]
}
---

# Scan a library whose folder cannot be reached

## Trigger

A scan starts while the library's root folder cannot be read.

## Outcome

The library is Unavailable and nothing in it is trashed; the next successful scan makes it Available again.
