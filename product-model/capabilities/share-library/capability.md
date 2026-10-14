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

# Share library

An Admin gives a user access to one library, or to every library including ones added later.
