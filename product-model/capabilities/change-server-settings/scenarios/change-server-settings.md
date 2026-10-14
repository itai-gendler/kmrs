---
{
  "kind": "primary",
  "routes": {
    "web": "Web UI"
  },
  "steps": [
    {
      "text": "The Admin changes settings and saves",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "server-settings",
          "effect": "reads",
          "facts": [
            "Delete empty collections",
            "Delete empty read lists",
            "Remember me duration",
            "Thumbnail size",
            "Task pool size",
            "Server port",
            "Context path",
            "Kobo proxy",
            "Kobo port",
            "Kepubify path",
            "Max upload size"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::settings"
        }
      }
    },
    {
      "text": "The Product saves the Server settings",
      "kind": "product",
      "entities": [
        {
          "entity": "server-settings",
          "effect": "changes",
          "facts": [
            "Delete empty collections",
            "Delete empty read lists",
            "Remember me duration",
            "Thumbnail size",
            "Task pool size",
            "Server port",
            "Context path",
            "Kobo proxy",
            "Kobo port",
            "Kepubify path",
            "Max upload size"
          ]
        }
      ],
      "actor": "admin",
      "contexts": {
        "web": {
          "place": "web::administration::settings"
        }
      }
    }
  ]
}
---

# Change server settings

## Trigger

An Admin opens Settings and saves changes.

## Outcome

The server uses the new settings; port and context path apply after a restart.

## Decision points

### Renew the remember-me key?

Did the Admin ask to renew the remember-me key?

- Yes → every remembered browser must sign in again.
- No → remembered browsers stay signed in.

## Edge cases

- A Remember me duration of 0 days or less is refused.
- A port or context path set in the configuration file or environment wins over the stored one.
