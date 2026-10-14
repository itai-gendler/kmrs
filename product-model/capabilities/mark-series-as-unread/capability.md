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
      "target": "crates/komga-server/src/api/series.rs#mark_series_as_unread"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/service/series.rs#delete_read_progress"
    }
  ]
}
---

# Mark series as unread

A User clears their progress on every book of one or several series.
