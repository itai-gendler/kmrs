---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User chooses Mark as read on a Series",
      "kind": "actor",
      "actor": "user",
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
      "text": "The Product records each Book of the Series not yet completed as Completed at its last page",
      "kind": "product",
      "entities": [
        {
          "entity": "read-progress",
          "effect": "creates",
          "facts": [
            "Page",
            "Read date"
          ],
          "to": "Completed"
        },
        {
          "entity": "book",
          "effect": "reads",
          "facts": []
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
          "place": "web::library::series"
        }
      }
    }
  ]
}
---

# Mark a series as read

## Trigger

A User chooses Mark as read on a series.

## Outcome

Every book of the series is Completed for that User.
