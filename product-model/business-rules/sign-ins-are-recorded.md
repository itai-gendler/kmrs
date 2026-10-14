---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "sign-in"
    },
    {
      "type": "capability",
      "id": "sync-kobo-library"
    },
    {
      "type": "entity",
      "id": "login-activity"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-server/src/auth/mod.rs#ApiKeyActivityThrottle"
    }
  ]
}
---

# Every sign-in attempt is recorded in login activity

Each sign-in, with a password, through an identity provider or with an API key, successful or failed, is recorded with when, where from, source and outcome. Successful uses of the same API key are recorded at most once an hour.
