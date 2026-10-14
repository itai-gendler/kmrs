---
{
  "availability": [
    {
      "place": "web::administration"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/settings.rs#update_server_settings"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/admin/settings/SettingsForm.tsx"
    }
  ]
}
---

# Change server settings

An Admin changes server-wide settings: automatic removal of empty collections and read lists, how long sign-ins are remembered, thumbnail size, task workers, server port and context path, Kobo proxy and port, kepubify path and upload size.
