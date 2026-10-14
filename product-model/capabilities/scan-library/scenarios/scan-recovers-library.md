---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin chooses Scan for an Unavailable Library",
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
      "text": "The Library's root folder can be read again",
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
      "text": "The Product marks the Library Available and finishes the scan",
      "kind": "product",
      "entities": [
        {
          "entity": "library",
          "effect": "changes",
          "facts": [],
          "from": "Unavailable",
          "to": "Available"
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

# Scan a library that was unavailable

## Trigger

A scan reaches the root folder of an Unavailable library again.

## Outcome

The library is Available again and its content follows its folder.
