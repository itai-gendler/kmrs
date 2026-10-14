---
{
  "availability": [
    {
      "place": "web::library"
    }
  ],
  "domain": "read-lists",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/readlists.rs#update_readlist_by_id"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/browse/AddToReadListDialog.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/readlists/BookPickerDialog.tsx"
    }
  ]
}
---

# Add book to read list

An Admin adds books to an existing read list, from a selection or from the read list itself.
