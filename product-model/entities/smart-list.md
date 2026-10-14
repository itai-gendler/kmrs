---
{
  "domain": "smart-lists",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "crates/komga-core/src/model/smart_list.rs#SmartList"
    }
  ]
}
---

# Smart list

Saved filters over books or series, evaluated live for whoever opens it.

## Information kept

- **Name** — unique among its owner's smart lists
- **Summary** — description
- **Target** — Books or Series
- **Filters** — the saved search conditions
- **Visibility** — Private, Public or Shared
- **Shared with** — the users a Shared list is visible to
