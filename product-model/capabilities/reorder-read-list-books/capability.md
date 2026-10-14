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
      "target": "webui/src/components/readlists/EditReadListBooks.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/readlists.rs#update_readlist_by_id"
    }
  ]
}
---

# Reorder read list books

An Admin drags the books of a manually ordered read list into a new reading order.
