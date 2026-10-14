---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin changes titles, status, summary, publisher, age rating, language, genres, tags, sharing labels or links and saves",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "series",
          "effect": "reads",
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
            "Alternate titles",
            "Locked fields"
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
      "text": "The Product saves the Series metadata and locks the edited fields",
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
            "Alternate titles",
            "Locked fields"
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

# Edit a series' metadata

## Trigger

An Admin chooses Edit metadata on a series.

## Outcome

The series shows the new values and the edited fields are locked.

## Edge cases

- Editing several selected series applies only the switched-on fields, locked by default.
- A language that is not a valid BCP 47 tag is refused.
