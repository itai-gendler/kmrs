---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User chooses Mark as unread on a Series",
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
      "text": "The Product deletes the User's Read progress on every Book of the Series",
      "kind": "product",
      "entities": [
        {
          "entity": "read-progress",
          "effect": "removes",
          "from": "Completed"
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

# Mark a series as unread

## Trigger

A User chooses Mark as unread on a series.

## Outcome

No book of the series has progress for that User.
