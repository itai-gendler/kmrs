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
      "target": "crates/komga-server/src/api/series.rs#update_series_metadata"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "webui/src/components/metadata/EditSeriesDialog.tsx"
    }
  ]
}
---

# Edit series metadata

An Admin edits the metadata of one or several series. Every edited field is locked so refreshes keep it.
