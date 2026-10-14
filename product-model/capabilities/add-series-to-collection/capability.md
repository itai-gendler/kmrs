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
      "target": "crates/komga-server/src/api/collections.rs#update_collection_by_id"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/browse/AddToCollectionDialog.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/collections/SeriesPickerDialog.tsx"
    }
  ]
}
---

# Add series to collection

An Admin adds series to an existing collection, from a selection or from the collection itself.
