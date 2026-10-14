---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "read-progress",
      "effect": "changes"
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
      "target": "crates/komga-server/src/api/books.rs#mark_progression"
    }
  ]
}
---

# Reading progress is changed only by its own user

Each User's progress moves only through their own reading, marking and devices.
