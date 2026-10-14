---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "create-api-key"
    },
    {
      "type": "capability",
      "id": "delete-api-key"
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

# An API key is shown once and its comment is unique

The secret is displayed only when the key is created; afterwards only its comment and dates are shown. A User's keys have distinct, non-blank comments.
