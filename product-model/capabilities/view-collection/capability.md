---
{
  "availability": [
    {
      "place": "web::library"
    }
  ],
  "domain": "collections",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/routes/detail/collection.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/collections.rs#get_series_by_collection_id"
    }
  ]
}
---

# View collection

A User opens a collection to see its series, in the collection's order when it is manually ordered.
