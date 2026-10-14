---
{
  "kind": "primary",
  "result": "achieved",
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
      "capability": "import-read-list",
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
      "capability": "import-read-list",
      "contexts": {
        "web": {
          "place": "web::administration::import-read-list"
        }
      }
    },
    {
      "text": "The Admin reads the new Read list",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "read-list",
          "effect": "reads",
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
      "capability": "view-read-list",
      "contexts": {
        "web": {
          "place": "web::library::read-list"
        }
      }
    }
  ]
}
---

# Import a read list and open it

## Trigger

An Admin imports a .cbl file.

## Outcome

The Admin is on the new read list and sees its books.
