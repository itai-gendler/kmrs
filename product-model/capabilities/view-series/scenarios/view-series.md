---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User opens a Series",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "series",
          "effect": "reads",
          "facts": [
            "Title",
            "Status",
            "Summary",
            "Publisher",
            "Age rating",
            "Genres",
            "Tags",
            "Links",
            "Book count"
          ]
        },
        {
          "entity": "book",
          "effect": "reads",
          "facts": [
            "Title",
            "Number"
          ]
        },
        {
          "entity": "read-progress",
          "effect": "reads",
          "facts": [
            "Page"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::library::series"
        }
      }
    }
  ]
}
---

# View a series

## Trigger

A User opens a series.

## Outcome

The User sees the series' metadata, its books in order and their reading state.

## Edge cases

- A series in a library the User may not access, or outside their content restrictions, is not found for them.
