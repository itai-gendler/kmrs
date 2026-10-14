---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "read-progress",
      "effect": "changes",
      "contexts": [
        {
          "place": "koreader-sync"
        }
      ]
    }
  ],
  "permits": [
    {
      "actors": [
        "user"
      ],
      "when": [
        {
          "entity": "user",
          "fact": "KOReader sync",
          "is": "On"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/admin/users/roles.ts"
    }
  ]
}
---

# KOReader syncs progress only for users with KOReader sync

KOReader keeps a user's reading progress only when they hold KOReader sync.
