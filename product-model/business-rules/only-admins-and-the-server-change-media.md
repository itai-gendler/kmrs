---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "book",
      "effect": "changes",
      "facts": [
        "Format",
        "Page count",
        "Media status"
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
      "unattended": true
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/books.rs#book_analyze"
    }
  ]
}
---

# Only admins and the server analyze books

Admins ask for analysis; the server analyzes new and changed books on its own.
