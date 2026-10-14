---
{
  "availability": [
    {
      "place": "web::library"
    },
    {
      "place": "web::administration"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/users.rs#update_my_password"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/users.rs#update_password_by_id"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/account/PasswordSection.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/admin/users/ChangePasswordDialog.tsx"
    }
  ]
}
---

# Change password

A User sets a new password for themselves from Security, or an Admin sets one for another user from Users.
