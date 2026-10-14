---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin chooses Scan or Scan (deep) for a Library",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "library",
          "effect": "reads",
          "facts": [
            "Name",
            "Root folder"
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
      "actor": "admin",
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

# Scan a library

## Trigger

An Admin chooses Scan for a library on Libraries.

## Outcome

The library's series and books match its folder again: new ones appear and vanished ones are Unavailable.

## Decision points

### Deep or regular scan?

Did the Admin choose Scan (deep)?

- Yes → every folder is read again whatever its modified time.
- No → unchanged folders are skipped.

## Edge cases

- Rows under folders that could not be read are left untouched until a later scan reads them.
- A trashed book or series whose files reappear, or that moved and still matches by size and hash, is restored with its metadata.
