---
{
  "kind": "validation",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin enters a name and a root folder",
      "kind": "actor",
      "actor": "admin",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::administration::libraries"
        }
      }
    },
    {
      "text": "The folder is missing, is not a folder, or contains or is contained in another Library's root folder",
      "kind": "condition",
      "entities": [
        {
          "entity": "library",
          "effect": "reads",
          "facts": [
            "Root folder"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::libraries"
        }
      }
    },
    {
      "text": "The Product refuses the new library",
      "kind": "product",
      "entities": [
        {
          "entity": "library",
          "effect": "reads",
          "facts": []
        }
      ],
      "actor": "admin",
      "contexts": {
        "web": {
          "place": "web::administration::libraries"
        }
      }
    }
  ]
}
---

# Add a library with an unusable root folder

## Trigger

An Admin adds a library whose root folder does not exist, is not a folder, or sits inside or around another library's.

## Outcome

No library is created; the Admin sees why the folder was refused.

## Edge cases

- A name another library already has is refused the same way.
