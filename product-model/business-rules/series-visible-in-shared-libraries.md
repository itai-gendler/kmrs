---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "series",
      "effect": "reads"
    }
  ],
  "permits": [
    {
      "actors": [
        "admin"
      ]
    },
    {
      "actors": [
        "user"
      ],
      "when": [
        {
          "entity": "user",
          "fact": "All libraries",
          "is": "On"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "contains",
          "entity": "library"
        },
        {
          "verb": "accesses",
          "entity": "user"
        }
      ]
    },
    {
      "unattended": true
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/restriction.rs#check_series_by_id"
    }
  ]
}
---

# A series is seen only by users its library is shared with

Admins see every library. A User sees a series when every library, or that series' library, is shared with them. Content restrictions narrow this further.
