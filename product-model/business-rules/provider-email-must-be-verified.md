---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "sign-in"
    },
    {
      "type": "context",
      "context": {
        "place": "web::public::sign-in"
      }
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/oauth2.rs#resolve_email"
    }
  ]
}
---

# Identity provider sign-in needs a verified email

An identity provider must return an email, and, for OpenID Connect providers, confirm it is verified unless the operator turned that check off; the email then has to match an account unless account creation is on.
