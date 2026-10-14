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
      "target": "crates/komga-server/src/api/collections.rs#delete_collection_by_id"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/routes/detail/collection.tsx"
    }
  ]
}
---

# Delete collection

An Admin deletes a collection; its series stay in their libraries.
