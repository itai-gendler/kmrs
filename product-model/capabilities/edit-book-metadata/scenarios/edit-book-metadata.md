---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin changes title, number, summary, release date, authors, tags, ISBN or links and saves",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "book",
          "effect": "reads",
          "facts": [
            "Title",
            "Number",
            "Sort number",
            "Summary",
            "Release date",
            "Authors",
            "Tags",
            "ISBN",
            "Links",
            "Locked fields"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::library::book"
        }
      }
    },
    {
      "text": "The Product saves the Book metadata and locks the edited fields",
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
            "Links",
            "Locked fields"
          ]
        }
      ],
      "actor": "admin",
      "contexts": {
        "web": {
          "place": "web::library::book"
        }
      }
    }
  ]
}
---

# Edit a book's metadata

## Trigger

An Admin chooses Edit metadata on a book.

## Outcome

The book shows the new values and the edited fields are locked.

## Edge cases

- Editing several selected books applies the switched-on shared fields to each, locked by default.
