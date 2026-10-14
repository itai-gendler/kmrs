---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin picks one of the Series' Posters",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "poster",
          "effect": "reads",
          "facts": [
            "Type",
            "Image"
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
          "place": "web::library::series"
        }
      }
    },
    {
      "text": "The Product makes that Poster the selected one",
      "kind": "product",
      "entities": [
        {
          "entity": "poster",
          "effect": "changes",
          "facts": [
            "Selected"
          ]
        }
      ],
      "actor": "admin",
      "contexts": {
        "web": {
          "place": "web::library::series"
        }
      }
    }
  ]
}
---

# Select a poster

## Trigger

An Admin picks one of a series' posters.

## Outcome

That poster is shown for the series everywhere.
