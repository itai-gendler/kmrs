---
{
  "kind": "edge",
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
      "text": "No Book, or more than one Book, has that KOReader hash",
      "kind": "condition",
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
      "text": "The Product refuses the progress",
      "kind": "product",
      "entities": [],
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

# KOReader syncs a document the server cannot match

## Trigger

KOReader sends progress for a document hash no book, or more than one book, has.

## Outcome

Nothing is recorded.
