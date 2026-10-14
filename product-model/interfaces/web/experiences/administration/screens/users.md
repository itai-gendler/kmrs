---
{
  "entities": [
    {
      "entity": "user",
      "shows": [
        "Email",
        "File download",
        "Page streaming",
        "Kobo sync",
        "KOReader sync",
        "Age restriction",
        "Allowed labels",
        "Excluded labels",
        "Shared libraries",
        "All libraries"
      ],
      "collects": [
        "Email",
        "Password",
        "File download",
        "Page streaming",
        "Kobo sync",
        "KOReader sync",
        "All libraries",
        "Shared libraries",
        "Age restriction",
        "Allowed labels",
        "Excluded labels"
      ]
    },
    {
      "entity": "login-activity",
      "shows": [
        "When",
        "Email",
        "IP",
        "Source",
        "Status",
        "Agent",
        "API key"
      ]
    },
    {
      "entity": "library",
      "shows": [
        "Name"
      ]
    }
  ],
  "entryPoints": [
    {
      "web": "/admin/users"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/routes/admin/users.tsx"
    }
  ]
}
---

# Users

Every account with its roles, library access, content restrictions and authentication activity.
