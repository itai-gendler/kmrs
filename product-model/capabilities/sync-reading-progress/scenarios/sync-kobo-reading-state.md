---
{
  "kind": "primary",
  "routes": {
    "kobo": "Kobo e-reader"
  },
  "steps": [
    {
      "text": "The User's Kobo e-reader reports its position in a Book",
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
        "kobo": {
          "place": "kobo-sync"
        }
      }
    },
    {
      "text": "The Product records the position as the User's Read progress on the Book",
      "kind": "product",
      "entities": [
        {
          "entity": "read-progress",
          "effect": "creates",
          "facts": [
            "Page",
            "Position",
            "Read date",
            "Device"
          ],
          "to": "In progress"
        },
        {
          "entity": "book",
          "effect": "reads",
          "facts": []
        }
      ],
      "actor": "user",
      "contexts": {
        "kobo": {
          "place": "kobo-sync"
        }
      }
    }
  ]
}
---

# A Kobo e-reader reports reading progress

## Trigger

The User reads a synced book on their Kobo e-reader.

## Outcome

The server's progress for that book follows the e-reader.

## Edge cases

- When the e-reader reports the book finished, the progress is put on its last position and Completed.
