---
{
  "availability": [
    {
      "place": "web::administration"
    }
  ],
  "domain": "users",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/users.rs#update_user"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/admin/users/UserFormDialog.tsx"
    }
  ]
}
---

# Stop sharing library

An Admin takes a user's access to a library away, or stops sharing every library with them.
