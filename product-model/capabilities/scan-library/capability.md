---
{
  "availability": [
    {
      "place": "web::administration"
    },
    {
      "place": "web::library"
    }
  ],
  "domain": "libraries",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/libraries.rs#library_scan"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/service/library_content.rs#scan_root_folder"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/service/scheduler.rs"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/admin/libraries/LibraryCard.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/layout/SidebarLibraryMenu.tsx"
    }
  ]
}
---

# Scan library

The server reads a library's root folder: new folders and files become series and books, files that disappeared move to the trash, and moved or returning files are recognised. Admins start a scan; libraries also scan on their own schedule and on startup.
