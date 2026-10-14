---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Library's scan interval elapsed, or the server started and the Library scans on startup",
      "kind": "condition",
      "entities": [
        {
          "entity": "library",
          "effect": "reads",
          "facts": [
            "Scan interval",
            "Scan on startup"
          ]
        }
      ],
      "unattended": true,
      "contexts": {
        "web": {
          "place": "web::administration::libraries"
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
      "contexts": {
        "web": {
          "place": "web::administration::libraries"
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
      "contexts": {
        "web": {
          "place": "web::administration::libraries"
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
      "contexts": {
        "web": {
          "place": "web::administration::libraries"
        }
      }
    }
  ]
}
---

# Scheduled scan

## Trigger

A library's scan interval elapses, or the server starts with Scan on startup turned on.

## Outcome

The library's series and books match its folder without anyone asking.
