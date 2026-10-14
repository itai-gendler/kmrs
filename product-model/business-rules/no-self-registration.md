---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "sign-in"
    },
    {
      "type": "capability",
      "id": "claim-server"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/koreader.rs#register_user"
    }
  ]
}
---

# There is no self-registration

Nobody creates their own account by signing up; KOReader's sign-up is always refused. Accounts come from claiming, from an Admin, or from a configured identity provider.
