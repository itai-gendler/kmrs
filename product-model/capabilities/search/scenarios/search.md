---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User enters a search query",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::library::search"
        }
      }
    },
    {
      "text": "The Product finds matching Series, Books, Collections and Read lists the User may see",
      "kind": "product",
      "entities": [
        {
          "entity": "series",
          "effect": "reads",
          "facts": [
            "Title"
          ]
        },
        {
          "entity": "book",
          "effect": "reads",
          "facts": [
            "Title"
          ]
        },
        {
          "entity": "collection",
          "effect": "reads",
          "facts": [
            "Name"
          ]
        },
        {
          "entity": "read-list",
          "effect": "reads",
          "facts": [
            "Name"
          ]
        }
      ],
      "actor": "user",
      "contexts": {
        "web": {
          "place": "web::library::search"
        }
      }
    },
    {
      "text": "The User reads the results grouped by kind",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "series",
          "effect": "reads",
          "facts": [
            "Title"
          ]
        },
        {
          "entity": "book",
          "effect": "reads",
          "facts": [
            "Title"
          ]
        },
        {
          "entity": "collection",
          "effect": "reads",
          "facts": [
            "Name"
          ]
        },
        {
          "entity": "read-list",
          "effect": "reads",
          "facts": [
            "Name"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::library::search"
        }
      }
    }
  ]
}
---

# Search the server

## Trigger

A User types a query in search.

## Outcome

The User sees matching series, books, collections and read lists.

## Edge cases

- Traditional and simplified Chinese match each other.
