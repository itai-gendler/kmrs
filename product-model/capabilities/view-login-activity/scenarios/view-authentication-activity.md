---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin opens the authentication activity on Users",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "login-activity",
          "effect": "reads",
          "facts": [
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
          "entity": "user",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::users"
        }
      }
    }
  ]
}
---

# Review every user's authentication activity

## Trigger

An Admin opens authentication activity on Users.

## Outcome

The Admin sees every sign-in attempt on the server, successful or failed, newest first.
