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
      "target": "crates/komga-server/src/auth/mod.rs#auth_middleware"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/oauth2.rs#callback"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/routes/login.tsx"
    }
  ]
}
---

# Sign in

A person signs in with their email and password, or through an identity provider the operator configured, and lands where they were going. Keep me signed in remembers them on that browser.
