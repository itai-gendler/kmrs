---
{
  "availability": [
    {
      "place": "web::library"
    }
  ],
  "domain": "api-keys",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/users.rs#delete_api_key"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/account/ApiKeysSection.tsx"
    }
  ]
}
---

# Delete API key

A User deletes one of their API keys; clients using it can no longer sign in with it.
