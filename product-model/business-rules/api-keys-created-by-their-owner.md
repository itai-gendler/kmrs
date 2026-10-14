---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "api-key",
      "effect": "creates"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "owns",
          "entity": "user"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/users.rs#create_api_key"
    }
  ]
}
---

# An API key is created by the user it acts for

Each User creates their own keys.
