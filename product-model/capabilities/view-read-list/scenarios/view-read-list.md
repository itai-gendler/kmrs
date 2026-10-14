---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The User opens a Read list",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "read-list",
          "effect": "reads",
          "facts": [
            "Name",
            "Summary",
            "Manual ordering",
            "Books"
          ]
        },
        {
          "entity": "book",
          "effect": "reads",
          "facts": [
            "Title",
            "Number"
          ]
        },
        {
          "entity": "read-progress",
          "effect": "reads",
          "facts": [
            "Page"
          ]
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

# View a read list

## Trigger

A User opens a read list.

## Outcome

The User sees the read list's summary and books with their reading state.
