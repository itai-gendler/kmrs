---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin chooses Delete files on a Series and confirms",
      "kind": "actor",
      "actor": "admin",
      "entities": [
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
      "text": "The Product deletes every Book file of the Series and its folder, and makes the Series and its Books Unavailable",
      "kind": "product",
      "entities": [
        {
          "entity": "series",
          "effect": "changes",
          "facts": [],
          "from": "Available",
          "to": "Unavailable"
        },
        {
          "entity": "book",
          "effect": "changes",
          "facts": [],
          "from": "Available",
          "to": "Unavailable"
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

# Delete a series' files

## Trigger

An Admin chooses Delete files on a series and confirms.

## Outcome

The series' files and folder are gone from disk and the series is Unavailable.
