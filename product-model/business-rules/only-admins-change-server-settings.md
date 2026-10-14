---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "server-settings",
      "effect": "changes"
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
      "target": "crates/komga-server/src/api/settings.rs#update_server_settings"
    }
  ]
}
---

# Only admins change server settings

Server-wide settings are an Admin's job.
