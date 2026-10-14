---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "read-progress",
      "effect": "removes"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "keeps",
          "entity": "user"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/books.rs#delete_book_read_progress"
    }
  ]
}
---

# Reading progress is cleared only by its own user

Marking as unread clears the User's own progress only.
