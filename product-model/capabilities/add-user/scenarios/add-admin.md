---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin enters the new user's email and password and turns on the Admin role",
      "kind": "actor",
      "actor": "admin",
      "entities": [
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
    },
    {
      "text": "The Product creates the User holding the Admin role",
      "kind": "product",
      "entities": [
        {
          "entity": "user",
          "effect": "creates",
          "facts": [
            "Email",
            "Password",
            "File download",
            "Page streaming",
            "Kobo sync",
            "KOReader sync",
            "All libraries",
            "Shared libraries",
            "Age restriction",
            "Allowed labels",
            "Excluded labels"
          ]
        },
        {
          "entity": "admin",
          "effect": "creates",
          "facts": [],
          "with": "user"
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

# Add a user with the Admin role

## Trigger

An Admin adds a user and turns on the Admin role.

## Outcome

The new User holds the Admin role, with full access including server settings.
