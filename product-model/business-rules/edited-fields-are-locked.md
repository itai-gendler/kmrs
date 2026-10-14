---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "edit-series-metadata"
    },
    {
      "type": "capability",
      "id": "edit-book-metadata"
    },
    {
      "type": "capability",
      "id": "refresh-metadata"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-media/src/metadata/patch.rs"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/metadata/fields.tsx"
    }
  ]
}
---

# Edited metadata fields are locked and refreshes keep them

Saving an edited field locks it; a metadata refresh changes only unlocked fields.
