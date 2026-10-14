---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin chooses Empty trash in the Library's sidebar actions",
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
          "place": "web::library"
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
          "place": "web::library"
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
          "place": "web::library"
        }
      }
    }
  ]
}
---

# Empty a library's trash from the sidebar

## Trigger

An Admin chooses Empty trash in a library's sidebar actions.

## Outcome

The library's Unavailable series and books are gone for good.
