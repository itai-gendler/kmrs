---
{
  "kind": "primary",
  "routes": {
    "opds": "OPDS client"
  },
  "steps": [
    {
      "text": "The User opens the OPDS catalog in their reader",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "opds": {
          "place": "opds"
        }
      }
    },
    {
      "text": "The Product lists the Libraries, Series, Collections, Read lists and Books the User may see, with how far they read",
      "kind": "product",
      "entities": [
        {
          "entity": "library",
          "effect": "reads",
          "facts": [
            "Name"
          ]
        },
        {
          "entity": "series",
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
        },
        {
          "entity": "book",
          "effect": "reads",
          "facts": [
            "Title",
            "Number",
            "Page count"
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
        "opds": {
          "place": "opds"
        }
      }
    },
    {
      "text": "The User navigates feeds or searches",
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
        }
      ],
      "contexts": {
        "opds": {
          "place": "opds"
        }
      }
    }
  ]
}
---

# Browse the OPDS catalog

## Trigger

A User adds the server's OPDS catalog to their reader with their email and password or an API key.

## Outcome

The reader lists what the User may access and offers each book to stream or download.

## Edge cases

- Both OPDS 1.2 and OPDS 2 catalogs are offered.
