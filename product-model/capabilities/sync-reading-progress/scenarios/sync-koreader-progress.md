---
{
  "kind": "primary",
  "routes": {
    "koreader": "KOReader"
  },
  "steps": [
    {
      "text": "KOReader sends the User's progress for a document hash",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "koreader": {
          "place": "koreader-sync"
        }
      }
    },
    {
      "text": "The Product finds the one Book with that KOReader hash",
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
        "koreader": {
          "place": "koreader-sync"
        }
      }
    },
    {
      "text": "The Product records the progress as the User's Read progress on the Book",
      "kind": "product",
      "entities": [
        {
          "entity": "read-progress",
          "effect": "changes",
          "facts": [
            "Page",
            "Position",
            "Read date",
            "Device"
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
        "koreader": {
          "place": "koreader-sync"
        }
      }
    }
  ]
}
---

# KOReader pushes reading progress

## Trigger

KOReader syncs progress for an open document.

## Outcome

The server's progress for the matching book follows KOReader.
