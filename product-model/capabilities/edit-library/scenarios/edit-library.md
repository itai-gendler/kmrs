---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin changes the Library's settings and saves",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "library",
          "effect": "reads",
          "facts": [
            "Name",
            "Root folder",
            "Oneshots directory",
            "Scan interval",
            "Scan on startup",
            "Scanned file types",
            "Directory exclusions",
            "Import sources",
            "Series cover",
            "Analysis options",
            "Empty trash after scan"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::libraries"
        }
      }
    },
    {
      "text": "The Product saves the Library's settings",
      "kind": "product",
      "entities": [
        {
          "entity": "library",
          "effect": "changes",
          "facts": [
            "Name",
            "Root folder",
            "Oneshots directory",
            "Scan interval",
            "Scan on startup",
            "Scanned file types",
            "Directory exclusions",
            "Import sources",
            "Series cover",
            "Analysis options",
            "Empty trash after scan"
          ]
        }
      ],
      "actor": "admin",
      "contexts": {
        "web": {
          "place": "web::administration::libraries"
        }
      }
    },
    {
      "text": "The Product reschedules periodic scans and queues the rescan or background work the change calls for",
      "kind": "product",
      "entities": [],
      "actor": "admin",
      "contexts": {
        "web": {
          "place": "web::administration::libraries"
        }
      }
    }
  ]
}
---

# Edit a library

## Trigger

An Admin chooses Edit library and saves changes.

## Outcome

The library uses its new settings; a rescan or background work follows where the change calls for it.

## Decision points

### Does the change need a rescan?

Is the root folder, oneshots directory, file types, exclusions or forced modified time different?

- Yes → the Product queues a scan of the library.
- No → nothing is rescanned.

### Was hashing, repair or conversion just turned on?

Did Hash files, Hash pages, Hash Koreader position, Repair extensions or Convert to CBZ go from off to on?

- Yes → the Product queues that work for the books that need it.
- No → no background work is queued.

## Edge cases

- The same folder and name checks as Add library apply against the other libraries.
