---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "A Read list has no Books left and Delete empty read lists is on",
      "kind": "condition",
      "entities": [
        {
          "entity": "read-list",
          "effect": "reads",
          "facts": [
            "Books"
          ]
        },
        {
          "entity": "server-settings",
          "effect": "reads",
          "facts": [
            "Delete empty read lists"
          ]
        },
        {
          "entity": "book",
          "effect": "reads",
          "facts": []
        }
      ],
      "unattended": true,
      "contexts": {
        "web": {
          "place": "web::library::read-list"
        }
      }
    },
    {
      "text": "The Product deletes the empty Read list",
      "kind": "product",
      "entities": [
        {
          "entity": "read-list",
          "effect": "removes"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::library::read-list"
        }
      }
    }
  ]
}
---

# An emptied read list is deleted

## Trigger

Books leave a read list because they were removed from the server while Delete empty read lists is on.

## Outcome

Read lists left without books are gone.
