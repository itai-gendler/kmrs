---
{
  "domain": "api-keys",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-core/src/model/user.rs#ApiKey"
    }
  ]
}
---

# API key

A key a User creates so third-party clients and e-readers can act as them.

## Information kept

- **Comment** — the User's label, unique among their keys
- **Key** — the secret, shown only when created
- **Created** — when it was created
- **Last used** — when a client last used it
- **Kobo sync point** — what the Kobo e-readers using it have already received
