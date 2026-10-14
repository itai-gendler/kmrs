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
      "target": "webui/src/components/collections/EditCollectionMembers.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/detail/MembershipRemoveButton.tsx"
    }
  ]
}
---

# Remove series from collection

An Admin takes series out of a collection; a collection always keeps at least one series.
