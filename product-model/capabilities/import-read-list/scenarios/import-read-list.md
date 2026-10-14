---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin chooses a .cbl file and Match against library",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "library",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::import-read-list"
        }
      }
    },
    {
      "text": "The Product matches each entry to Books by series and number",
      "kind": "product",
      "entities": [
        {
          "entity": "book",
          "effect": "reads",
          "facts": [
            "Title",
            "Number"
          ]
        },
        {
          "entity": "series",
          "effect": "reads",
          "facts": [
            "Title"
          ]
        }
      ],
      "actor": "admin",
      "contexts": {
        "web": {
          "place": "web::administration::import-read-list"
        }
      }
    },
    {
      "text": "The Admin picks a Book for entries with several matches, names the Read list and chooses Create read list",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "book",
          "effect": "reads",
          "facts": [
            "Title",
            "Number"
          ]
        },
        {
          "entity": "read-list",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::import-read-list"
        }
      }
    },
    {
      "text": "The Product creates a manually ordered Read list of the matched Books and opens it",
      "kind": "product",
      "entities": [
        {
          "entity": "read-list",
          "effect": "creates",
          "facts": [
            "Name",
            "Summary",
            "Manual ordering",
            "Books"
          ]
        },
        {
          "entity": "book",
          "effect": "reads",
          "facts": []
        }
      ],
      "actor": "admin",
      "contexts": {
        "web": {
          "place": "web::administration::import-read-list"
        }
      }
    }
  ]
}
---

# Import a ComicRack read list

## Trigger

An Admin opens Import readlist and chooses a .cbl file.

## Outcome

A manually ordered read list holds the matched books in the file's order, and the Admin is on it.

## Edge cases

- A name another read list already has is flagged before creating.
