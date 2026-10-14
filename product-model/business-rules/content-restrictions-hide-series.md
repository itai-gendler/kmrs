---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "browse-series"
    },
    {
      "type": "capability",
      "id": "view-series"
    },
    {
      "type": "capability",
      "id": "browse-books"
    },
    {
      "type": "capability",
      "id": "view-book"
    },
    {
      "type": "capability",
      "id": "read-book"
    },
    {
      "type": "capability",
      "id": "search"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-core/src/model/user.rs#is_content_allowed"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/restriction.rs#check_metadata"
    }
  ]
}
---

# Content restrictions hide series outside a user's age rating and labels

With Allow only, a series needs an age rating at or below the age; with allowed labels, it needs one of them; when both are set, either one admits it. Exclude hides series rated at or above the age, and excluded labels always hide. The books of a hidden series are hidden with it, and collections and read lists show only the members that remain.
