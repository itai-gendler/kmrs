---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User enters a new password twice and chooses Update password",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::library::security"
        }
      }
    },
    {
      "text": "The Product replaces the User's password",
      "kind": "product",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Password"
          ]
        }
      ],
      "actor": "user",
      "contexts": {
        "web": {
          "place": "web::library::security"
        }
      }
    }
  ]
}
---

# Change one's own password

## Trigger

A User opens Security and fills in Change password.

## Outcome

The User's password is the new one and they stay signed in on this device.

## Edge cases

- Two entries that differ are refused with Passwords do not match before anything is sent.
- A blank password is refused.
