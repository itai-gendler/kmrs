---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "read-progress",
      "effect": "creates"
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
      "target": "crates/komga-server/src/api/books.rs#mark_book_read_progress"
    }
  ]
}
---

# Reading progress is started only by its own user

Each User has their own progress; nobody starts progress for someone else.
