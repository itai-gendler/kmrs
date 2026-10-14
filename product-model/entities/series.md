---
{
  "relations": [
    {
      "entity": "book",
      "verb": "contains",
      "cardinality": "one-to-many"
    },
    {
      "entity": "poster",
      "verb": "has",
      "cardinality": "one-to-many"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-core/src/model/series.rs#SeriesMetadata"
    }
  ]
}
---

# Series

A folder of books in a library, or a single book in the oneshots directory, with its own metadata.

## Information kept

- **Title** — shown everywhere; taken from the folder name or imported metadata
- **Sort title** — the title used for sorting
- **Status** — Ongoing, Ended, Abandoned or Hiatus
- **Summary** — description
- **Reading direction** — Left to right, Right to left, Vertical or Webtoon
- **Publisher** — publisher name
- **Age rating** — minimum age; content restrictions compare against it
- **Language** — a BCP 47 tag
- **Genres** — genre names
- **Tags** — free tags
- **Total book count** — how many books the series has in total
- **Sharing labels** — labels that users' allowed and excluded labels compare against
- **Links** — titled web links
- **Alternate titles** — labelled other titles
- **Locked fields** — which fields metadata refreshes leave alone
- **Folder** — where the series lives on disk
- **Oneshot** — whether it is a single book shown as its own series
- **Book count** — how many books it holds

## States

### Available

Its folder was found at the last scan.

### Unavailable

Its folder disappeared or its files were deleted; it waits in the library's trash.
