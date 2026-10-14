---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "book",
      "effect": "reads",
      "contexts": [
        {
          "place": "kobo-sync"
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
          "fact": "Kobo sync",
          "is": "On"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/kobo.rs"
    }
  ]
}
---

# Kobo e-readers sync only for users with Kobo sync

A Kobo e-reader reaches the server only with the API key of a user holding Kobo sync, Admins included.
