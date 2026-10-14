---
{
  "entities": [
    {
      "entity": "user",
      "collects": [
        "Email",
        "Password"
      ]
    }
  ],
  "entryPoints": [
    {
      "web": "/login"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/routes/login.tsx"
    }
  ]
}
---

# Sign in

The sign-in page; on a server without accounts it offers to claim the server instead.
