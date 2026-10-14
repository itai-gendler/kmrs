---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "claim-server"
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
      "target": "crates/komga-server/src/api/claim.rs#claim"
    }
  ]
}
---

# A server is claimed once

Claiming creates the first account and is refused as soon as any account exists. The claimer gets every role and every library.
