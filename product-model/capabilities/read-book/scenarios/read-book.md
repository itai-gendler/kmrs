---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User chooses Read or Continue on a Book",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "book",
          "effect": "reads",
          "facts": [
            "Title",
            "Media status"
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
      "text": "The Product opens the reader at the User's saved page",
      "kind": "product",
      "entities": [
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
          "place": "web::library::reader"
        }
      }
    },
    {
      "text": "The User turns the pages of the Book",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "book",
          "effect": "reads",
          "facts": [
            "Page images",
            "Page count"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::library::reader"
        }
      }
    },
    {
      "text": "The Product saves the page reached as the User's Read progress",
      "kind": "product",
      "entities": [
        {
          "entity": "read-progress",
          "effect": "creates",
          "facts": [
            "Page",
            "Read date"
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
        "web": {
          "place": "web::library::reader"
        }
      }
    },
    {
      "text": "The Product marks the Read progress Completed when the User reaches the last page",
      "kind": "product",
      "entities": [
        {
          "entity": "read-progress",
          "effect": "changes",
          "facts": [
            "Page",
            "Read date"
          ],
          "from": "In progress",
          "to": "Completed"
        }
      ],
      "actor": "user",
      "contexts": {
        "web": {
          "place": "web::library::reader"
        }
      }
    }
  ]
}
---

# Read a book

## Trigger

A User chooses Read or Continue on a book.

## Outcome

The User reads the book; their progress follows the last page they reached and the book is Completed at its last page.

## Decision points

### Which reader?

Is the book an EPUB with reflowable text?

- Yes → the EPUB reader saves the position within the text.
- No → the comic reader saves the page number.

## Edge cases

- Reading from a read list keeps Previous and Next within that read list.
