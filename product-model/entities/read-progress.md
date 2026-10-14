---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-core/src/model/read_progress.rs#ReadProgress"
    }
  ]
}
---

# Read progress

How far one User got in one Book, wherever they read it.

## Information kept

- **Page** — the page reached
- **Position** — the position within an EPUB's text
- **Read date** — when it last changed
- **Device** — the device that reported it

## States

### In progress

The User started the book and has not reached its last page.

### Completed

The User reached the last page or marked the book as read.
