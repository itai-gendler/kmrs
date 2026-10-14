---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "scan-library"
    },
    {
      "type": "capability",
      "id": "empty-trash"
    },
    {
      "type": "capability",
      "id": "delete-library"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/service/library_content.rs#scan_root_folder"
    }
  ]
}
---

# Missing files go to the trash, not away

A scan never removes what it cannot find: vanished series and books become Unavailable and come back, metadata included, when their files return. Only emptying the trash removes them, and deleting a library never touches files on disk.
