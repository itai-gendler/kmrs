---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User opens Read lists",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "read-list",
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
      "text": "The Product lists the Read lists holding Books the User may see",
      "kind": "product",
      "entities": [
        {
          "entity": "read-list",
          "effect": "reads",
          "facts": [
            "Name",
            "Books"
          ]
        },
        {
          "entity": "book",
          "effect": "reads",
          "facts": []
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
      "text": "The User reads the Read lists and their book counts",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "read-list",
          "effect": "reads",
          "facts": [
            "Name",
            "Books"
          ]
        },
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
    }
  ]
}
---

# Browse read lists

## Trigger

A User opens Read lists.

## Outcome

The User sees each read list with the number of books they may see in it.
