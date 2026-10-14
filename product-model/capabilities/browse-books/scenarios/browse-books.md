---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User opens Books and sets filters or sort",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "book",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::library::library"
        }
      }
    },
    {
      "text": "The Product lists the Books the User may see with the User's Read progress",
      "kind": "product",
      "entities": [
        {
          "entity": "book",
          "effect": "reads",
          "facts": [
            "Title",
            "Number",
            "Media status"
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
      "actor": "user",
      "contexts": {
        "web": {
          "place": "web::library::library"
        }
      }
    },
    {
      "text": "The User reads the Books and how far they got",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "book",
          "effect": "reads",
          "facts": [
            "Title",
            "Number",
            "Media status"
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
      "contexts": {
        "web": {
          "place": "web::library::library"
        }
      }
    }
  ]
}
---

# Browse books

## Trigger

A User opens Books for a library or for all libraries.

## Outcome

The User sees the books they may access, with their reading state.
