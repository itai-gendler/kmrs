---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin changes the User's roles, age restriction, allowed labels or excluded labels and saves",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Email",
            "File download",
            "Page streaming",
            "Kobo sync",
            "KOReader sync",
            "Age restriction",
            "Allowed labels",
            "Excluded labels"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::users"
        }
      }
    },
    {
      "text": "The Product saves the User's permissions and signs them out of every session",
      "kind": "product",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "File download",
            "Page streaming",
            "Kobo sync",
            "KOReader sync",
            "Age restriction",
            "Allowed labels",
            "Excluded labels"
          ]
        }
      ],
      "actor": "admin",
      "contexts": {
        "web": {
          "place": "web::administration::users"
        }
      }
    }
  ]
}
---

# Change a user's roles and content restrictions

## Trigger

An Admin edits a user and changes their roles, age restriction or labels.

## Outcome

The user's new permissions apply and every session they had is signed out.

## Edge cases

- A label is kept in lower case and blank labels are dropped; a label both allowed and excluded stays only excluded.
