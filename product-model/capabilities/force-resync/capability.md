---
{
  "availability": [
    {
      "place": "web::library"
    }
  ],
  "domain": "api-keys",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/syncpoints.rs#delete_sync_points_for_current_user"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/account/ApiKeysSection.tsx"
    }
  ]
}
---

# Force resync

A User makes the devices that use one of their API keys, or all of them, receive their whole library again on the next sync.
