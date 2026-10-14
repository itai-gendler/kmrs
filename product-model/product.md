---
id: kmrs
summary: A comic & manga server in a single static Rust binary, drop-in compatible with Komga — same API, same database.
category: media-server
tags: [comics, manga, self-hosted, opds, e-readers]
authors:
  - name: everpcpc
license: MIT
languages: [en, de, es, fr, it, ja, ko, ru, zh-Hans, zh-Hant]
limitations:
  - There is no self-registration; accounts come from claiming the server, from an Admin, or from an identity provider the operator configured.
  - Collections and read lists are curated by Admins; other users browse and read them but never change them.
  - Deleting a library never deletes files on disk; only Delete file and Delete files remove book files.
  - Kobo e-readers receive only EPUB books.
  - Its data directory stays openable by Komga; data only kmrs keeps, such as smart lists, lives in a separate database.
---

# kmrs

kmrs serves comics, manga and books from folders on your own hardware. It scans library folders into series and books,
reads their metadata, and lets the people an Admin invites browse, search and read them in the bundled web UI, in OPDS
readers, on Kobo e-readers and in KOReader, with reading progress kept per person across all of them. Admins decide who
sees which library and what age ratings and labels they may see, curate collections and read lists, and edit metadata
and posters. kmrs is a drop-in replacement for Komga: same port, same API and the same database.

## Intent

*Keep Manga Reading Simple.* Your whole library, served from your own hardware and readable anywhere, from a single
binary that takes over an existing Komga installation's data directory without migration and keeps every client that
spoke to it working.
