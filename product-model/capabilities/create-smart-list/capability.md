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
      "target": "crates/komga-server/src/api/smartlists.rs#create_smart_list"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/smartlists/SmartListDialog.tsx"
    }
  ]
}
---

# Create smart list

A User saves filters over books or series as a named smart list they own. Lists other users create stay private.
