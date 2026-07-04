# Roza lesson feed (public)

This repository is the **over-the-air content feed** for the Roza iPad app. It contains
**only lesson data** — no source code.

- `manifest.json` — the list of gold lessons (bilingual, interactive) plus a
  `contentVersion` number. The app fetches this file, and when `contentVersion` is newer
  than what it has, it merges any new/updated lessons into the Library. No app rebuild.

The iPad app points at:
```
https://raw.githubusercontent.com/<owner>/<this-repo>/main/manifest.json
```

**Do not edit by hand.** This repo is published automatically from the private Roza
project via `publish.sh` (which regenerates `manifest.json` from the source-of-truth gold
lessons). Editing here directly would be overwritten on the next publish.
