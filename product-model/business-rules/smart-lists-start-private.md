---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "smart-list",
      "effect": "creates",
      "facts": [
        "Visibility"
      ]
    }
  ],
  "permits": [
    {
      "actors": [
        "admin"
      ]
    },
    {
      "actors": [
        "user"
      ],
      "when": [
        {
          "fact": "Visibility",
          "is": "Private"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/smartlists.rs#create_smart_list"
    }
  ]
}
---

# Users create only private smart lists

Anyone signed in creates smart lists; only an Admin creates one that is Public or Shared.
