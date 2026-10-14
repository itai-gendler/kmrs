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
      "target": "webui/src/components/collections/EditCollectionMembers.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/collections.rs#update_collection_by_id"
    }
  ]
}
---

# Reorder collection series

An Admin drags the series of a manually ordered collection into a new order.
