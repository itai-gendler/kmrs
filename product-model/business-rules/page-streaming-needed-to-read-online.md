---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "book",
      "effect": "reads",
      "facts": [
        "Page images"
      ]
    }
  ],
  "permits": [
    {
      "actors": [
        "admin"
      ]
    },
    {
      "actors": [
        "user"
      ],
      "when": [
        {
          "entity": "user",
          "fact": "Page streaming",
          "is": "On"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/books.rs#get_book_page_by_number"
    }
  ]
}
---

# Reading pages online needs Page streaming

Pages are served to Admins and to users with Page streaming.
