# CyberSim Facilitator Materials — Releases Guide

This document explains how facilitator materials are versioned and distributed, and how to publish updates.

---

## How distribution works

Facilitator materials are published as **GitHub Releases** — versioned snapshots with PDF files attached as downloadable assets. Each release captures a consistent set of materials at a point in time.

Two types of links are available for every file:

**A "latest" link** — always points to the most recent release, no matter what version that is:
```
https://github.com/cocitizen/cybersim-resources/releases/latest/download/FILENAME.pdf
```
The CyberSim website uses these links. They never need updating when a new release is published.

**A versioned link** — permanent, always points to that specific release:
```
https://github.com/cocitizen/cybersim-resources/releases/download/v1.1/FILENAME.pdf
```
Old versioned links work forever, even after newer releases exist. Use these if you need to share a specific version of a document.

> **Important:** The "latest" link only works if the filename stays identical between releases. Do not rename files between versions — the link will break. Settle on a filename before the first release and keep it.

---

## File naming convention

```
cybersim-{scenario}-{language}-{type}.pdf
```

Examples:
- `cybersim-cso-en-facilitator-guide.pdf`
- `cybersim-cso-en-participant-handout.pdf`
- `cybersim-campaign-en-facilitator-guide.pdf`
- `cybersim-parliament-fr-scenario-cards.pdf`

**Scenario codes:** `campaign`, `cso`, `parliament`, `observers`
**Language codes:** ISO 639-1 two-letter codes (`en`, `fr`, `es`, `ar`, etc.)

---

## Version numbering

Releases are tagged `v{major}.{minor}` — e.g. `v1.2`.

- **Major version** (`v2.0`) — significant scenario changes, restructured content
- **Minor version** (`v1.1`) — corrections, formatting updates, translation additions

If scenarios are on significantly different update cycles, per-scenario tags are fine: `cso-v1.2`, `campaign-v2.0`.

---

## How to publish a new release

1. Prepare all updated PDF files with the correct filenames (see naming convention above)
2. Go to [github.com/cocitizen/cybersim-resources](https://github.com/cocitizen/cybersim-resources)
3. Click **Releases** → **Draft a new release**
4. Set the tag: `v1.1` (create new tag)
5. Write brief release notes — what changed, which scenarios, which languages
6. Attach all PDF files for this release
7. Click **Publish release**

The website's "latest" links update automatically. No website changes needed.

---

## How to link from the website

Use the `latest` URL pattern for all website download links:

```
https://github.com/cocitizen/cybersim-resources/releases/latest/download/cybersim-cso-en-facilitator-guide.pdf
```

When building cybersim.app, these URLs can be embedded directly as download button `href` values.
