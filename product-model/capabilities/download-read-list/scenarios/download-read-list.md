---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User chooses Download on a Read list",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "read-list",
          "effect": "reads",
          "facts": [
            "Name"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::library::read-list"
        }
      }
    },
    {
      "text": "The Product sends one archive with the file of every Book of the Read list the User may see",
      "kind": "product",
      "entities": [
        {
          "entity": "book",
          "effect": "reads",
          "facts": [
            "File"
          ]
        },
        {
          "entity": "read-list",
          "effect": "reads",
          "facts": []
        }
      ],
      "actor": "user",
      "contexts": {
        "web": {
          "place": "web::library::read-list"
        }
      }
    }
  ]
}
---

# Download a read list

## Trigger

A User chooses Download on a read list.

## Outcome

The User has one archive with the read list's book files they may access.
