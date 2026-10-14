---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "book",
      "effect": "changes",
      "to": "Unavailable"
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
      "target": "crates/komga-server/src/service/book.rs#delete_book_files"
    }
  ]
}
---

# Only admins and scans make books Unavailable

A book becomes Unavailable when an Admin deletes its file or a scan finds it gone.
