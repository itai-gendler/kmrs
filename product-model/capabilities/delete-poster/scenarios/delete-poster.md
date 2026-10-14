---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin deletes an uploaded Poster of the Series",
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
      "text": "The Product deletes the Poster",
      "kind": "product",
      "entities": [
        {
          "entity": "poster",
          "effect": "removes"
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

# Delete an uploaded poster

## Trigger

An Admin deletes one of a series' uploaded posters.

## Outcome

The poster is gone; another poster is shown.

## Edge cases

- Generated and sidecar posters cannot be deleted.
