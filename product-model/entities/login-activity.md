---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-core/src/model/user.rs#AuthenticationActivity"
    }
  ]
}
---

# Login activity

Each attempt to sign in, with a password, a session, an identity provider or an API key, successful or not.

## Information kept

- **When** — date and time
- **Email** — the account or email tried
- **Source** — Password, API key or the identity provider
- **IP** — where the attempt came from
- **Agent** — the client's user agent
- **Status** — Success or Failed, with the reason
- **API key** — the API key's comment, when one was used
