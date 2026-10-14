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
      "target": "crates/komga-server/src/api/libraries.rs#add_library"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/service/library.rs#add_library"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/admin/libraries/LibraryDialog.tsx"
    }
  ]
}
---

# Add library

An Admin adds a library: a name and a root folder on the server, with scanning, import and analysis options. The new library is scanned right away.
