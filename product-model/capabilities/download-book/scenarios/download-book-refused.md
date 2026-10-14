---
{
  "kind": "validation",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User asks for a Book's file",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "book",
          "effect": "reads",
          "facts": [
            "Title"
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
      "text": "The User does not have File download",
      "kind": "condition",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "File download"
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
      "text": "The Product refuses to send the Book's file",
      "kind": "product",
      "entities": [
        {
          "entity": "book",
          "effect": "reads",
          "facts": []
        }
      ],
      "actor": "user",
      "contexts": {
        "web": {
          "place": "web::library::book"
        }
      }
    }
  ]
}
---

# Download a book without File download

## Trigger

A User without File download asks for a book's file.

## Outcome

No file is sent.
