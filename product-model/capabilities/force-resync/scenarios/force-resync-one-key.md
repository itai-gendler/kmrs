---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User chooses Force resync for an API key and confirms",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "api-key",
          "effect": "reads",
          "facts": [
            "Comment"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::library::api-keys"
        }
      }
    },
    {
      "text": "The Product forgets what devices using that API key already received",
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

# Force a resync for one API key

## Trigger

A User chooses Force resync for one of their API keys.

## Outcome

The next Kobo sync with that key receives everything again.
