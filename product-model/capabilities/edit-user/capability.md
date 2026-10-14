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

# Edit user

An Admin changes another user's roles and content restrictions. Any change of permissions signs that user out everywhere.
