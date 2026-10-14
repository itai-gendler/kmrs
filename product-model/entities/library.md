---
{
  "domain": "libraries",
  "relations": [
    {
      "entity": "series",
      "verb": "contains",
      "cardinality": "one-to-many"
    },
    {
      "entity": "book",
      "verb": "contains",
      "cardinality": "one-to-many"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-core/src/model/library.rs#Library"
    }
  ]
}
---

# Library

A root folder on the server whose sub-folders and files become series and books.

## Information kept

- **Name** — unique among libraries
- **Root folder** — absolute folder on the machine running the server
- **Oneshots directory** — books in folders whose path contains it become oneshots; empty disables it
- **Scan interval** — Disabled, Hourly, Every 6h, Every 12h, Daily or Weekly
- **Scan on startup** — whether the library is scanned when the server starts
- **Scanned file types** — whether CBX/CBR, PDF and EPUB files are picked up
- **Directory exclusions** — folder names skipped during scans
- **Import sources** — which of ComicInfo, EPUB, Mylar, local artwork and barcode ISBN metadata is read into series and books
- **Series cover** — which book's cover a series shows: First, First unread or first, First unread or last, or Last
- **Analysis options** — Hash files, Hash pages, Hash Koreader position, Analyze dimensions, Repair extensions and Convert to CBZ
- **Empty trash after scan** — whether what a scan makes Unavailable is removed right away

## States

### Available

Its root folder could be read at the last scan.

### Unavailable

Its root folder could not be read at the last scan; its content is kept as it was.
