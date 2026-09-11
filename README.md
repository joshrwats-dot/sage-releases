# SAGE releases

This repository exists to serve two things over HTTPS:

- **`feed/manifest.json`** — what the SAGE app reads when someone chooses
  *SAGE ▸ Check for Updates…*. It names one build: its version, the commit it
  was built from, where to download it, and the SHA-256 of that download.
- **the builds themselves**, attached to this repository's releases.

SAGE's source code is not here and is not public.

## What SAGE is, and who this is for

SAGE is a local-first assistant for macOS, in private testing. It is not
released, not for sale, and not supported. If you have found this repository
without being handed a build, there is nothing here you need.

## What a build is

Every archive served here is signed with a Developer ID, notarized by Apple,
and stapled, so it opens on a normal Mac without disabling anything. The
manifest's `archive_sha256` is checked by the app before an update is
installed, and the app verifies the downloaded bundle's signature itself.

## Not here on purpose

No telemetry, no analytics, and no crash reporting. The app does not check for
updates on its own: the only two things that check are the *Check for Updates…*
menu item and the `sage update check` command, both of which a person runs.

One thing that is not ours to refuse: GitHub counts downloads of release
assets, and the owner of this repository can see those counts.
