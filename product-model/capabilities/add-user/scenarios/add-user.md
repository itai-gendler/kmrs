---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin enters an email and a password, picks roles, library access and content restrictions",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "library",
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
      "text": "The Product creates the User",
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

# Add a user

## Trigger

An Admin chooses Add user.

## Outcome

The new User can sign in with the given email and password and reaches the libraries shared with them.

## Edge cases

- Library access left unset shares every library.
- An age below 0 is refused.
- An email that is not well formed or a blank password is refused.
