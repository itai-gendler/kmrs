---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User chooses Resync all devices and confirms",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::library::api-keys"
        }
      }
    },
    {
      "text": "The Product forgets what the devices using each of the User's API keys already received",
      "kind": "product",
      "entities": [
        {
          "entity": "api-key",
          "effect": "changes",
          "facts": [
            "Kobo sync point"
          ]
        }
      ],
      "actor": "user",
      "contexts": {
        "web": {
          "place": "web::library::api-keys"
        }
      }
    }
  ]
}
---

# Resync all devices

## Trigger

A User chooses Resync all devices.

## Outcome

The next Kobo sync with any of the User's keys receives everything again.
