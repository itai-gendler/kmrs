---
{
  "kind": "primary",
  "routes": {
    "koreader": "KOReader"
  },
  "steps": [
    {
      "text": "KOReader asks for the User's progress on a document hash",
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
      "text": "The Product returns the User's Read progress on the matching Book",
      "kind": "product",
      "entities": [
        {
          "entity": "read-progress",
          "effect": "reads",
          "facts": [
            "Page",
            "Position",
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

# KOReader fetches reading progress

## Trigger

KOReader asks for the server's progress of an open document.

## Outcome

KOReader can jump to where the User left off elsewhere.
