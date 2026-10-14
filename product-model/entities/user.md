---
{
  "kind": "person",
  "acts": "external",
  "domain": "users",
  "relations": [
    {
      "entity": "admin",
      "verb": "holds",
      "cardinality": "one-to-one"
    },
    {
      "entity": "library",
      "verb": "accesses",
      "cardinality": "many-to-many"
    },
    {
      "entity": "read-progress",
      "verb": "keeps",
      "cardinality": "one-to-many"
    },
    {
      "entity": "api-key",
      "verb": "owns",
      "cardinality": "one-to-many"
    },
    {
      "entity": "smart-list",
      "verb": "owns",
      "cardinality": "one-to-many"
    },
    {
      "entity": "login-activity",
      "verb": "has",
      "cardinality": "one-to-many"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-core/src/model/user.rs#KomgaUser"
    }
  ]
}
---

# User

A person with an account on the server. What they reach depends on the libraries shared with them, their roles and their content restrictions.

## Information kept

- **Email** — the address they sign in with; unique on the server, ignoring case
- **Password** — the secret checked when they sign in with email and password
- **File download** — role: whether they may download book files
- **Page streaming** — role: whether they may read book pages online
- **Kobo sync** — role: whether their Kobo e-readers may sync with the server
- **KOReader sync** — role: whether KOReader may sync their reading progress
- **All libraries** — whether every library, including ones added later, is shared with them
- **Shared libraries** — the libraries shared with them one by one
- **Age restriction** — None, Allow only content rated at or below an age, or Exclude content rated from an age
- **Allowed labels** — sharing labels; when set, series without one of them are hidden unless the age restriction admits them
- **Excluded labels** — sharing labels whose series are always hidden from them
