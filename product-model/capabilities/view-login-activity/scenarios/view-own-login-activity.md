---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User opens Security and reads their login activity",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "login-activity",
          "effect": "reads",
          "facts": [
            "When",
            "IP",
            "Source",
            "Status",
            "Agent"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::library::security"
        }
      }
    }
  ]
}
---

# Review one's own login activity

## Trigger

A User opens Security.

## Outcome

The User sees each sign-in to their account, newest first, with when, IP, source, status and agent.
