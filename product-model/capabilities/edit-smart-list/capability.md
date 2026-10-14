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

# Edit smart list

The owner of a smart list, or an Admin, changes its name, summary, target and filters.
