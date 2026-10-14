---
{
  "availability": [
    {
      "place": "web::library"
    }
  ],
  "domain": "read-lists",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/routes/detail/readlist.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/readlists.rs#get_books_by_readlist_id"
    }
  ]
}
---

# View read list

A User opens a read list to see its books, in reading order when it is manually ordered.
