---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "A Collection has no Series left and Delete empty collections is on",
      "kind": "condition",
      "entities": [
        {
          "entity": "collection",
          "effect": "reads",
          "facts": [
            "Series"
          ]
        },
        {
          "entity": "server-settings",
          "effect": "reads",
          "facts": [
            "Delete empty collections"
          ]
        },
        {
          "entity": "series",
          "effect": "reads",
          "facts": []
        }
      ],
      "unattended": true,
      "contexts": {
        "web": {
          "place": "web::library::collection"
        }
      }
    },
    {
      "text": "The Product deletes the empty Collection",
      "kind": "product",
      "entities": [
        {
          "entity": "collection",
          "effect": "removes"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::library::collection"
        }
      }
    }
  ]
}
---

# An emptied collection is deleted

## Trigger

Series leave a collection because they were removed from the server while Delete empty collections is on.

## Outcome

Collections left without series are gone.
