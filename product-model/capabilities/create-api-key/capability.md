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
      "target": "crates/komga-server/src/api/users.rs#create_api_key"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/account/ApiKeysSection.tsx"
    }
  ]
}
---

# Create API key

A User creates a key that third-party clients, Kobo e-readers and KOReader use to act as them.
