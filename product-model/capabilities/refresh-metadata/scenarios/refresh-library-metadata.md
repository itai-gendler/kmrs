---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin chooses Refresh metadata for a Library",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "library",
          "effect": "reads",
          "facts": [
            "Name",
            "Import sources"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::libraries"
        }
      }
    },
    {
      "text": "The Product reads metadata from the Library's import sources and updates every unlocked Book and Series field",
      "kind": "product",
      "entities": [
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
        },
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
          "entity": "library",
          "effect": "reads",
          "facts": []
        }
      ],
      "actor": "admin",
      "contexts": {
        "web": {
          "place": "web::administration::libraries"
        }
      }
    }
  ]
}
---

# Refresh a library's metadata

## Trigger

An Admin chooses Refresh metadata in a library's actions.

## Outcome

Unlocked metadata of every book and series in the library follows the library's import sources again.
