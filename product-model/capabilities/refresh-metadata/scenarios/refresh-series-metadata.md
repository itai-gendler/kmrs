---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin chooses Refresh metadata on a Series",
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
      "text": "The Product updates every unlocked field of the Series and its Books from their files",
      "kind": "product",
      "entities": [
        {
          "entity": "series",
          "effect": "changes",
          "facts": [
            "Title",
            "Sort title",
            "Status",
            "Summary",
            "Reading direction",
            "Publisher",
            "Age rating",
            "Language",
            "Genres",
            "Tags",
            "Total book count",
            "Sharing labels",
            "Links",
            "Alternate titles"
          ]
        },
        {
          "entity": "book",
          "effect": "changes",
          "facts": [
            "Title",
            "Number",
            "Sort number",
            "Summary",
            "Release date",
            "Authors",
            "Tags",
            "ISBN",
            "Links"
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

# Refresh a series' metadata

## Trigger

An Admin chooses Refresh metadata on a series.

## Outcome

The series' unlocked metadata follows its files and import sources again.
