---
{
  "availability": [
    {
      "place": "web::library"
    }
  ],
  "domain": "smart-lists",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/smartlists.rs#update_smart_list_by_id"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/smartlists/SmartListDialog.tsx"
    }
  ]
}
---

# Stop sharing smart list

An Admin removes users from the people a Shared smart list is shared with.
