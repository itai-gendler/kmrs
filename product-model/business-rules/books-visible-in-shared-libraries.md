---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "book",
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
      "target": "crates/komga-server/src/api/restriction.rs#check_book"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-core/src/model/user.rs#can_access_library"
    }
  ]
}
---

# A book is seen only by users its library is shared with

Admins see every library. A User sees a book when every library, or that book's library, is shared with them. Content restrictions narrow this further.
