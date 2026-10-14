---
{
  "availability": [
    {
      "place": "web::library"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/routes/dashboard.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/dashboard/sections.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/books.rs#get_books_on_deck"
    }
  ]
}
---

# View dashboard

A User sees what to read next across their libraries or within one: Keep Reading, On Deck and the recently released, added, updated and read rows.
