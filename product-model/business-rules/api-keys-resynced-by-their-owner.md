---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "api-key",
      "effect": "changes"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "owns",
          "entity": "user"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/syncpoints.rs#delete_sync_points_for_current_user"
    }
  ]
}
---

# An API key's sync is reset by its owner or by its own syncs

Only the key's owner forces a resync; the key's own Kobo syncs move its sync point forward.
