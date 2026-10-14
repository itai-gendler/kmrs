---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "book",
      "effect": "changes",
      "facts": [
        "Title",
        "Number",
        "Sort number",
        "Summary",
        "Release date",
        "Authors",
        "Tags",
        "ISBN",
        "Links"
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
      "target": "crates/komga-server/src/api/books.rs#update_book_metadata"
    }
  ]
}
---

# Only admins and the server's refreshes change book metadata

Admins edit book metadata; scans, analysis and refreshes update it from the files.
