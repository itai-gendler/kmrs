---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "create-collection"
    },
    {
      "type": "capability",
      "id": "remove-series-from-collection"
    },
    {
      "type": "capability",
      "id": "rename-collection"
    },
    {
      "type": "capability",
      "id": "create-read-list"
    },
    {
      "type": "capability",
      "id": "remove-book-from-read-list"
    },
    {
      "type": "capability",
      "id": "edit-read-list"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/dto/collection.rs#unique_violations"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/service/collection.rs#add_collection"
    }
  ]
}
---

# Collections and read lists always hold at least one member and have unique names

A collection keeps at least one series and a read list at least one book; to empty one, delete it. Names are unique among collections and among read lists.
