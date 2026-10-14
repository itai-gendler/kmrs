---
{
  "type": "api",
  "actors": [
    "user"
  ],
  "entryPoints": [
    {
      "api": "/opds/v1.2/catalog"
    },
    {
      "api": "/opds/v2/catalog"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/opds_v1.rs#router"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/api/opds_v2.rs#router"
    }
  ]
}
---

# OPDS catalog

OPDS 1.2 and OPDS 2 catalogs for e-book and comic reader apps, with page streaming and downloads; readers sign in with email and password or an API key.
