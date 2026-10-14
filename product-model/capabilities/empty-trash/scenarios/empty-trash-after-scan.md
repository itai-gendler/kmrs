---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "A scan of a Library with Empty trash after scan finished",
      "kind": "condition",
      "entities": [
        {
          "entity": "library",
          "effect": "reads",
          "facts": [
            "Empty trash after scan"
          ]
        }
      ],
      "unattended": true,
      "contexts": {
        "web": {
          "place": "web::administration::libraries"
        }
      }
    },
    {
      "text": "The Product removes the Library's Unavailable Series with all their Books",
      "kind": "product",
      "entities": [
        {
          "entity": "series",
          "effect": "removes",
          "from": "Unavailable"
        },
        {
          "entity": "book",
          "effect": "removes",
          "from": "Unavailable",
          "as": "in-series",
          "with": "series"
        },
        {
          "entity": "library",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::libraries"
        }
      }
    },
    {
      "text": "The Product removes the Library's other Unavailable Books",
      "kind": "product",
      "entities": [
        {
          "entity": "book",
          "effect": "removes",
          "from": "Unavailable",
          "as": "loose"
        },
        {
          "entity": "library",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::libraries"
        }
      }
    }
  ]
}
---

# Empty the trash after a scan

## Trigger

A scan of a library with Empty trash after scan finishes.

## Outcome

What the scan made Unavailable is removed at once.
