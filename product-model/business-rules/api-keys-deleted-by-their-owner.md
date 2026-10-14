---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "api-key",
      "effect": "removes"
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
      "target": "crates/komga-server/src/api/users.rs#delete_api_key"
    }
  ]
}
---

# An API key is deleted by its owner

A User deletes only their own keys.
