---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "delete-collection"
    },
    {
      "type": "capability",
      "id": "delete-read-list"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/service/collection.rs#delete_empty_collections"
    }
  ]
}
---

# Empty collections and read lists are removed when the settings say so

With Delete empty collections or Delete empty read lists on, a collection or read list left empty after a scan or after emptying the trash is deleted.
