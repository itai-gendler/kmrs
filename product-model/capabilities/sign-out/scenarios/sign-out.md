---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User chooses Sign out",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::library"
        }
      }
    },
    {
      "text": "The Product ends the session and forgets the browser",
      "kind": "product",
      "entities": [],
      "actor": "user",
      "contexts": {
        "web": {
          "place": "web::library"
        }
      }
    }
  ]
}
---

# Sign out

## Trigger

A signed-in User chooses Sign out.

## Outcome

The session on this browser has ended and the sign-in page is shown.
