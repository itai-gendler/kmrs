---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin chooses Scan in the Library's sidebar actions",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "library",
          "effect": "reads",
          "facts": [
            "Name"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::library"
        }
      }
    },
    {
      "text": "The Product adds a Series for each new folder, with a Book for each of its files",
      "kind": "product",
      "entities": [
        {
          "entity": "series",
          "effect": "creates",
          "facts": [
            "Title",
            "Folder",
            "Oneshot"
          ],
          "to": "Available"
        },
        {
          "entity": "book",
          "effect": "creates",
          "facts": [
            "Title",
            "Number",
            "File name",
            "File",
            "File size",
            "Oneshot",
            "Added",
            "Media status"
          ],
          "to": "Available",
          "as": "first",
          "with": "series"
        }
      ],
      "actor": "admin",
      "contexts": {
        "web": {
          "place": "web::library"
        }
      }
    },
    {
      "text": "The Product adds a Book for each new file in an existing Series",
      "kind": "product",
      "entities": [
        {
          "entity": "book",
          "effect": "creates",
          "facts": [
            "Title",
            "Number",
            "File name",
            "File",
            "File size",
            "Oneshot",
            "Added",
            "Media status"
          ],
          "to": "Available",
          "as": "added"
        },
        {
          "entity": "series",
          "effect": "reads",
          "facts": []
        }
      ],
      "actor": "admin",
      "contexts": {
        "web": {
          "place": "web::library"
        }
      }
    },
    {
      "text": "The Product makes Books whose files are gone Unavailable",
      "kind": "product",
      "entities": [
        {
          "entity": "book",
          "effect": "changes",
          "facts": [],
          "from": "Available",
          "to": "Unavailable",
          "as": "vanished"
        }
      ],
      "actor": "admin",
      "contexts": {
        "web": {
          "place": "web::library"
        }
      }
    }
  ]
}
---

# Scan a library from the sidebar

## Trigger

An Admin opens a library's actions in the sidebar and chooses Scan.

## Outcome

The scan is queued and the library's content follows its folder.
