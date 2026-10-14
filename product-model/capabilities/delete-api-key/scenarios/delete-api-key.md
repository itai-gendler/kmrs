---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User chooses Delete API key for one of their keys",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "api-key",
          "effect": "reads",
          "facts": [
            "Comment",
            "Created",
            "Last used"
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
      "text": "The Product deletes the API key",
      "kind": "product",
      "entities": [
        {
          "entity": "api-key",
          "effect": "removes"
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

# Delete an API key

## Trigger

A User chooses Delete API key next to one of their keys.

## Outcome

The key is gone and requests that present it are refused.
