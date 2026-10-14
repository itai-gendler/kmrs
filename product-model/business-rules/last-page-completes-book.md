---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "read-book"
    },
    {
      "type": "capability",
      "id": "mark-book-as-read"
    },
    {
      "type": "capability",
      "id": "mark-series-as-read"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/books.rs#mark_read_progress"
    }
  ]
}
---

# Reaching the last page completes a book

Progress on the last page is Completed; marking as read records the last page.
