---
{
  "relations": [
    {
      "entity": "read-progress",
      "verb": "has",
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
      "target": "crates/komga-core/src/model/book.rs#BookMetadata"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-core/src/model/media.rs#Media"
    }
  ]
}
---

# Book

One comic, manga or e-book file in a series.

## Information kept

- **Title** — shown everywhere
- **Number** — its number in the series as shown
- **Sort number** — the number used for ordering
- **Summary** — description
- **Release date** — when it was published
- **Authors** — names with roles such as writer or penciller
- **Tags** — free tags
- **ISBN** — its ISBN
- **Links** — titled web links
- **Locked fields** — which fields metadata refreshes leave alone
- **File name** — the file's name; admins also see its full path
- **File** — the file itself, as downloaded
- **File size** — size of the file
- **Format** — CBZ, CBR, PDF, EPUB and the like
- **Page count** — number of pages
- **Page images** — the pages served for reading online
- **Media status** — To be analyzed, Ready, Error, Unsupported or Outdated
- **Oneshot** — whether it is shown as its own series
- **Added** — when the server first found it

## States

### Available

Its file was found at the last scan.

### Unavailable

Its file disappeared or was deleted; it waits in the library's trash and cannot be read.
