---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin chooses Empty trash for a Library",
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
      "actor": "admin",
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

# Empty a library's trash

## Trigger

An Admin chooses Empty trash for a library.

## Outcome

The library's Unavailable series and books are gone for good.

## Edge cases

- With Delete empty collections or Delete empty read lists turned on, collections and read lists left empty are removed too.
