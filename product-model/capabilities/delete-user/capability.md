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
      "target": "crates/komga-server/src/api/users.rs#delete_user"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-db/src/dao/user.rs#delete"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/admin/users/DeleteUserDialog.tsx"
    }
  ]
}
---

# Delete user

An Admin permanently removes another user together with their reading progress, API keys and sessions.
