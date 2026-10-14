---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User opens Collections",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "collection",
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
      "text": "The Product lists the Collections holding Series the User may see",
      "kind": "product",
      "entities": [
        {
          "entity": "collection",
          "effect": "reads",
          "facts": [
            "Name",
            "Series"
          ]
        },
        {
          "entity": "series",
          "effect": "reads",
          "facts": []
        }
      ],
      "actor": "user",
      "contexts": {
        "web": {
          "place": "web::library::library"
        }
      }
    },
    {
      "text": "The User reads the Collections and their series counts",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "collection",
          "effect": "reads",
          "facts": [
            "Name",
            "Series"
          ]
        },
        {
          "entity": "series",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::library::library"
        }
      }
    }
  ]
}
---

# Browse collections

## Trigger

A User opens Collections.

## Outcome

The User sees each collection with the number of series they may see in it.
