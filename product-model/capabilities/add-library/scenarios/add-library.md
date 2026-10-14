---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin enters a name and a root folder and sets the scanning, import and analysis options",
      "kind": "actor",
      "actor": "admin",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::administration::libraries"
        }
      }
    },
    {
      "text": "The Product creates the Library and queues its first scan",
      "kind": "product",
      "entities": [
        {
          "entity": "library",
          "effect": "creates",
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
          ],
          "to": "Available"
        }
      ],
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

# Add a library

## Trigger

An Admin chooses Add library.

## Outcome

The library exists and its first scan is queued.
