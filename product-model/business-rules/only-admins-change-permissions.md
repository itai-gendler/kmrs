---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "user",
      "effect": "changes",
      "facts": [
        "File download",
        "Page streaming",
        "Kobo sync",
        "KOReader sync",
        "Age restriction",
        "Allowed labels",
        "Excluded labels",
        "All libraries",
        "Shared libraries"
      ]
    }
  ],
  "permits": [
    {
      "actors": [
        "admin"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/users.rs#update_user"
    }
  ]
}
---

# Only admins change a user's roles, library access and content restrictions

Roles, library access and content restrictions are set by an Admin, never by the user, and never by an Admin on their own account.
