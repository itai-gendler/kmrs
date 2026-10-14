---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "browse-smart-lists"
    },
    {
      "type": "capability",
      "id": "view-smart-list"
    },
    {
      "type": "capability",
      "id": "change-smart-list-visibility"
    },
    {
      "type": "capability",
      "id": "stop-sharing-smart-list"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/service/smart_list.rs#is_visible_to"
    }
  ]
}
---

# A smart list is seen by its owner, admins and the people its visibility admits

Private lists are seen by their owner and Admins, Public lists by everyone, Shared lists also by the chosen users. Names are unique per owner, and a Shared list always names at least one user. What a list matches is limited to what the viewer may see.
