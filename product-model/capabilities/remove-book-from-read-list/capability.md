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
      "target": "crates/komga-server/src/api/readlists.rs#update_readlist_by_id"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/readlists/EditReadListBooks.tsx"
    }
  ]
}
---

# Remove book from read list

An Admin takes books out of a read list; a read list always keeps at least one book.
