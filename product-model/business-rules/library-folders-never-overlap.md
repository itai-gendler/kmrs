---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "add-library"
    },
    {
      "type": "capability",
      "id": "edit-library"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/service/library.rs#check_library_validity"
    }
  ]
}
---

# Library root folders exist and never nest

A library's root folder must exist and be a folder, must not lie inside another library's root folder or contain one, and its name must be unique.
