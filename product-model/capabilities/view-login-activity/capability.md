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
      "target": "crates/komga-server/src/api/users.rs#my_authentication_activity"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/users.rs#authentication_activity"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/account/ActivitySection.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/admin/users/ActivitySection.tsx"
    }
  ]
}
---

# View login activity

A User reviews the sign-ins to their own account; an Admin reviews the authentication activity of every user.
