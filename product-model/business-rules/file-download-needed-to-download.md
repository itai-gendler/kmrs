---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "book",
      "effect": "reads",
      "facts": [
        "File"
      ]
    }
  ],
  "permits": [
    {
      "actors": [
        "admin"
      ]
    },
    {
      "actors": [
        "user"
      ],
      "when": [
        {
          "entity": "user",
          "fact": "File download",
          "is": "On"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/books.rs#download_book_file_internal"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/series.rs#download_series_as_zip"
    }
  ]
}
---

# Downloading files needs File download

Book files, series archives and read list archives are sent to Admins and to users with File download.
