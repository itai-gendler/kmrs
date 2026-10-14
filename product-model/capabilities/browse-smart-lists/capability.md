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
      "target": "webui/src/routes/browse/smartlists.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/smartlists.rs#get_smart_lists"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/service/smart_list.rs#is_visible_to"
    }
  ]
}
---

# Browse smart lists

A User browses the smart lists they own and those shared with them; an Admin may browse everyone's.
