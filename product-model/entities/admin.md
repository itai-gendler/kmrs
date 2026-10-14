---
{
  "kind": "person",
  "acts": "external",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-core/src/model/user.rs#is_admin"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/auth/mod.rs#require_role"
    }
  ]
}
---

# Admin

A User holding the Admin role: full access, including libraries, users, metadata, curated lists and server settings. Admins reach every library and hold every role's permissions, except Kobo sync, which they need like anyone else.
