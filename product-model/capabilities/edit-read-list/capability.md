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
      "target": "webui/src/routes/detail/readlist.tsx"
    }
  ]
}
---

# Edit read list

An Admin changes a read list's name and summary.
