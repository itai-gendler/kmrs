---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "user",
      "effect": "creates"
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
        "visitor"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/users.rs#create_user"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/claim.rs#claim"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/oauth2.rs#callback"
    }
  ]
}
---

# Admins add users; a claim or a provider sign-in creates an account

Admins add users. Otherwise an account is created only when the first person claims an unclaimed server, or when someone signs in through an identity provider with an email no account has and the operator turned on account creation.
