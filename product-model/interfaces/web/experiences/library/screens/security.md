---
{
  "entities": [
    {
      "entity": "login-activity",
      "shows": [
        "When",
        "IP",
        "Source",
        "Status",
        "Agent"
      ]
    },
    {
      "entity": "user",
      "collects": [
        "Password"
      ]
    }
  ],
  "entryPoints": [
    {
      "web": "/account/security"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/routes/account/security.tsx"
    }
  ]
}
---

# Security

The person's password and login activity.
