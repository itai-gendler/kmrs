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
      "target": "webui/src/routes/detail/smartlist.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/smartlists.rs#get_books_by_smart_list_id"
    }
  ]
}
---

# View smart list

A User opens a smart list to see the books or series its saved filters match right now.
