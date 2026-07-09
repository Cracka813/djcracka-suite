# DJ Cracka Software Suite

Public file feed for the DJ Cracka Utility Suite — a set of Windows PowerShell tools for DJs and streamers, built for [Cracka.gg](https://cracka.gg).

This repository hosts the small, plainly-readable files each tool checks against. In keeping with the suite's "visible, never obfuscated" licensing stance, everything here is public and readable by a simple HTTP GET — no token or credential is needed to read.

## Files

| File | Purpose |
|---|---|
| `Cracka_Suite_License.json` | The license registry. Each tool validates against this array of entries. |
| `version.json` | Current version of each tool, for update checks. |
| `CNAME` | GitHub Pages custom-domain record (`license.cracka.dev`). |

## Served at

```
https://license.cracka.dev/Cracka_Suite_License.json
https://license.cracka.dev/version.json
```

Every tool's `$LICENSE_URL` already points at the address above.

## Notes

- Reading these files needs nothing — they are public static files served over HTTPS via GitHub Pages.
- Writing to them automatically (e.g. a future Fourthwall/Make.com signup flow) is a separate, more sensitive path that requires a GitHub Personal Access Token with repo-write scope, used through GitHub's API — not a plain URL fetch.
- To point every tool at a new URL at once, use the License Manager tool's "Update License URL Across Scripts" option.

_Part of the DJ Cracka Utility Suite._
