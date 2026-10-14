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

# Change smart list visibility

An Admin makes a smart list Private, Public or Shared with chosen users.
