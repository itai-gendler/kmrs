---
{
  "kind": "validation",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User enters a comment",
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
      "text": "One of the User's API keys already has that comment",
      "kind": "condition",
      "entities": [
        {
          "entity": "api-key",
          "effect": "reads",
          "facts": [
            "Comment"
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
          "place": "web::library::api-keys"
        }
      }
    },
    {
      "text": "The Product refuses the new key",
      "kind": "product",
      "entities": [],
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

# Create an API key with a comment already used

## Trigger

A User submits a comment one of their keys already has.

## Outcome

No key is created.

## Edge cases

- A blank comment is refused.
