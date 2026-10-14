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
      "target": "crates/komga-server/src/api/collections.rs#create_collection"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/service/collection.rs#add_collection"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/browse/AddToCollectionDialog.tsx"
    }
  ]
}
---

# Create collection

An Admin starts a new collection from selected series.
