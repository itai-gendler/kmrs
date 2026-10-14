---
{
  "availability": [
    {
      "place": "web::administration"
    }
  ],
  "domain": "libraries",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/libraries.rs#delete_library_by_id"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/service/library.rs#delete_library"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/admin/libraries/DeleteLibraryDialog.tsx"
    }
  ]
}
---

# Delete library

An Admin removes a library with all of its series and books from the server. Files on disk are not deleted.
