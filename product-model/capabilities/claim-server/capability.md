---
{
  "availability": [
    {
      "place": "web::public"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/claim.rs#claim"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/routes/login.tsx"
    }
  ]
}
---

# Claim server

The first person to open a new server creates its administrator account and is signed in with it. Claiming is offered only while the server has no account at all.
