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
      "target": "crates/komga-server/src/api/users.rs#create_user"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/admin/users/UserFormDialog.tsx"
    }
  ]
}
---

# Add user

An Admin gives someone access to the server with an email, a password, roles, library access and content restrictions.
