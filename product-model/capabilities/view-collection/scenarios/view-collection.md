---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User opens a Collection",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "collection",
          "effect": "reads",
          "facts": [
            "Name",
            "Manual ordering",
            "Series"
          ]
        },
        {
          "entity": "series",
          "effect": "reads",
          "facts": [
            "Title"
          ]
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

# View a collection

## Trigger

A User opens a collection.

## Outcome

The User sees the collection's series they may see.

## Edge cases

- Series the User may not see are left out; the collection still shows.
