---
scope: The server's sign-in, users, libraries, scanning, browsing, reading, curation, OPDS and Kobo/KOReader sync code, and the web UI pages over it.
method: Static reading of the Rust server, the React web UI and their locale strings; nothing was run.
covered:
  - description: Authentication, sessions, claim, sign-in through identity providers and logout.
    paths: [crates/komga-server/src/auth/, crates/komga-server/src/api/claim.rs, crates/komga-server/src/api/login.rs, crates/komga-server/src/api/oauth2.rs]
  - description: User accounts, API keys, login activity and Kobo sync point reset endpoints.
    paths: [crates/komga-server/src/api/users.rs, crates/komga-server/src/api/syncpoints.rs, crates/komga-server/src/service/user.rs]
  - description: Library endpoints, library service, scanning, trash and scan scheduling.
    paths: [crates/komga-server/src/api/libraries.rs, crates/komga-server/src/service/library.rs, crates/komga-server/src/service/library_content.rs, crates/komga-server/src/service/scheduler.rs]
  - description: Series and book endpoints and services, read progress, access and content restriction checks.
    paths: [crates/komga-server/src/api/series.rs, crates/komga-server/src/api/books.rs, crates/komga-server/src/api/restriction.rs, crates/komga-server/src/service/series.rs, crates/komga-server/src/service/book.rs]
  - description: Collections, read lists and smart lists endpoints and services.
    paths: [crates/komga-server/src/api/collections.rs, crates/komga-server/src/api/readlists.rs, crates/komga-server/src/api/smartlists.rs, crates/komga-server/src/service/collection.rs, crates/komga-server/src/service/readlist.rs, crates/komga-server/src/service/smart_list.rs]
  - description: OPDS 1.2 and OPDS 2 catalogs.
    paths: [crates/komga-server/src/api/opds_v1.rs, crates/komga-server/src/api/opds_v2.rs]
  - description: Kobo sync, KOReader sync and sync points.
    paths: [crates/komga-server/src/api/kobo.rs, crates/komga-server/src/api/koreader.rs, crates/komga-server/src/service/sync_point.rs]
  - description: Server settings endpoint.
    paths: [crates/komga-server/src/api/settings.rs, crates/komga-server/src/settings.rs]
  - description: Domain model types and metadata application with field locks.
    paths: [crates/komga-core/src/model/, crates/komga-media/src/metadata/]
  - description: Search index.
    paths: [crates/komga-search/]
  - description: Web UI routes, layout, browse, detail, reader, metadata, curation, account and administration components for the mapped areas.
    paths: [webui/src/router.tsx, webui/src/routes/, webui/src/components/layout/, webui/src/components/browse/, webui/src/components/detail/, webui/src/components/media/, webui/src/components/reader/, webui/src/components/metadata/, webui/src/components/collections/, webui/src/components/readlists/, webui/src/components/smartlists/, webui/src/components/account/, webui/src/components/admin/libraries/, webui/src/components/admin/users/, webui/src/components/admin/settings/, webui/src/components/dashboard/, webui/src/lib/]
exclusions:
  - description: Database migrations, schema dump and data access layer.
    paths: [crates/komga-db/]
  - description: Development tasks, the differential test harness, CI, packaging and the docs redirect page.
    paths: [xtask/, tests/, .github/, Dockerfile, Cross.toml, .cargo/, pages-redirect/]
  - description: Operational endpoints, OpenAPI document, logging, profiling and HTTP plumbing.
    paths: [crates/komga-server/src/api/actuator.rs, crates/komga-server/src/api/openapi.rs, crates/komga-server/resources/, crates/komga-server/src/logging.rs, crates/komga-server/src/profiling.rs, crates/komga-server/src/http/, crates/komga-server/src/service/metrics.rs]
  - description: Web UI design system primitives.
    paths: [webui/src/components/ui/]
unmapped:
  - description: The external metadata-matching integration endpoints, service and admin pages.
    paths: [crates/komga-server/src/api/komf.rs, crates/komga-server/src/service/komf.rs, webui/src/components/admin/komf/, webui/src/components/KomfJobsPanel.tsx]
  - description: Reading trackers sync.
    paths: [crates/komga-server/src/service/tracker_sync.rs, webui/src/components/trackers/]
  - description: Page hashes, duplicate pages and duplicate files.
    paths: [crates/komga-server/src/api/page_hashes.rs, crates/komga-server/src/service/page_hash.rs, webui/src/components/admin/page-hashes/, webui/src/components/admin/duplicates/]
  - description: Importing book files from outside libraries and transient books.
    paths: [crates/komga-server/src/service/import.rs, crates/komga-server/src/api/transient_books.rs, crates/komga-server/src/service/transient_book.rs]
  - description: Reading statistics.
    paths: [crates/komga-server/src/api/stats.rs, crates/komga-server/src/service/reading_stats.rs]
  - description: Historical events, task queue, maintenance and server status.
    paths: [crates/komga-server/src/api/history.rs, crates/komga-server/src/api/tasks.rs, crates/komga-server/src/service/tasks.rs, crates/komga-server/src/service/maintenance.rs, webui/src/components/admin/server/]
  - description: Release checks, announcements, fonts, client and UI settings, pinned libraries and dashboard sections.
    paths: [crates/komga-server/src/api/releases.rs, crates/komga-server/src/api/announcements.rs, crates/komga-server/src/api/fonts.rs, crates/komga-server/src/api/client_settings.rs]
  - description: Referential values, filesystem browsing, book conversion, kepub conversion and the Kobo store proxy.
    paths: [crates/komga-server/src/api/referential.rs, crates/komga-server/src/api/filesystem.rs, crates/komga-server/src/service/convert.rs, crates/komga-server/src/service/kepub.rs, crates/komga-server/src/service/kobo_proxy.rs]
  - description: Server-sent events, webhooks, thumbnails generation, web publication manifests and configuration loading.
    paths: [crates/komga-server/src/sse/, crates/komga-server/src/webhook.rs, crates/komga-server/src/events.rs, crates/komga-server/src/thumbnails.rs, crates/komga-server/src/webpub.rs, crates/komga-server/src/config/, crates/komga-server/src/service/metadata.rs]
  - description: Media analyzers, scanner and readers for archive, PDF and EPUB files.
    paths: [crates/komga-media/src/analyzer.rs, crates/komga-media/src/container.rs, crates/komga-media/src/detect.rs, crates/komga-media/src/hash.rs, crates/komga-media/src/image.rs, crates/komga-media/src/kepubify.rs, crates/komga-media/src/pdf.rs, crates/komga-media/src/rar.rs, crates/komga-media/src/scanner.rs, crates/komga-media/src/zip.rs]
limitations: []
---

# Coverage
