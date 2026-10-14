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
      "target": "crates/komga-server/src/api/libraries.rs#update_library_by_id"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/service/library.rs#update_library"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/admin/libraries/LibraryDialog.tsx"
    }
  ]
}
---

# Edit library

An Admin changes a library's name, root folder and options. Changes that affect which files belong to it trigger a rescan, and newly enabled hashing, repair or conversion queue work for existing books.
