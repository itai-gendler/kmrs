---
{
  "availability": [
    {
      "place": "web::administration"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/readlists.rs#match_comic_rack_list"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/routes/import/readlist.tsx"
    }
  ]
}
---

# Import read list

An Admin turns a ComicRack .cbl file into a read list: entries are matched against the libraries, the Admin settles ambiguous ones, and unmatched entries are skipped.
