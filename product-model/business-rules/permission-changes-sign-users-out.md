---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "edit-user"
    },
    {
      "type": "capability",
      "id": "share-library"
    },
    {
      "type": "capability",
      "id": "stop-sharing-library"
    },
    {
      "type": "capability",
      "id": "change-password"
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

# Changing a user's permissions signs them out everywhere

When an Admin changes a user's roles, library access or content restrictions, every session that user has ends, so the new permissions apply at once. Setting another user's password signs them out too; changing one's own password keeps the current session.
