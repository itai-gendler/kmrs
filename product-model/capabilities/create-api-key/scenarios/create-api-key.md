---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User enters a comment such as KOReader on Boox",
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
      "text": "The Product creates an API key for the User and shows the key once",
      "kind": "product",
      "entities": [
        {
          "entity": "api-key",
          "effect": "creates",
          "facts": [
            "Comment",
            "Key",
            "Created"
          ]
        },
        {
          "entity": "user",
          "effect": "reads",
          "facts": []
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

# Create an API key

## Trigger

A User chooses New API key on API keys.

## Outcome

The User has a new key labelled with their comment; the key itself is shown this once.
