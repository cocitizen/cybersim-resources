# CyberSim Resources — Releases Guide

This document explains how to create frozen release packets for CyberSim resources.

Most routine updates do **not** need a GitHub Release. For everyday use, the latest approved printable files live in each scenario’s `current/` folder.

Use a GitHub Release only when we need to preserve the exact set of materials used for a specific event, workshop, pilot, translation milestone, partner handoff, or other meaningful checkpoint.

Releases should use a **ZIP file** containing the resource packet for that event or milestone.

## Normal workflow without a release

For ordinary updates:

1. Edit the relevant source files in `source/`.
2. Export a new PDF.
3. Replace the matching exported PDF in `current/`.
4. Replace or update the matching source files in `source/`.
5. Commit the PDF and source file changes together with a short note.

That is enough for normal ongoing work.

## What a release means

A release is a frozen ZIP packet of files for a specific purpose.

It answers questions like:

- What exact files did we use for the July 2026 CSO workshop?
- Which version of the role cards went with a specific pilot?
- What packet did we send to a partner or facilitator group?
- What materials were current at a major milestone?

A release does **not** need to be created for every typo fix, formatting update, or routine file replacement.

## Tags and releases

GitHub Releases are built on top of Git tags.

A **tag** marks the exact state of the repository at a particular moment.

A **release** is a downloadable resource packet connected to that tag and accompanied by notes.

In practical terms:

```text
Tag = a marker for the exact state of the repository at that moment
Release = a downloadable resource packet connected to that tag, with notes
```

When you create a GitHub Release and type a new tag name, GitHub creates the tag for you. Most contributors do not need to create tags separately.

For CyberSim resources, the release page is what people will usually use. The tag is there to preserve the repository state that the release is connected to.

Example:

```text
Tag: cso-2026-07-workshop
Release title: CSO July 2026 Workshop Resource Packet
Attached file: cybersim-cso-en-resource-packet-2026-07-workshop.zip
```

One important detail: a tag marks the state of the **whole repository**, not just one scenario folder. That is okay. Just make the release notes clear about what the release is actually for.

For example:

```markdown
This release freezes the CSO English resource packet for the July 2026 workshop. Other scenario folders may exist in the same repository but are not part of this release packet.
```

## Release assets and repository files

The ZIP file attached to a GitHub Release is called a release asset.

Release assets are stored by GitHub, but they are not normal files inside the repository folders.

That means there are two related things:

```text
Repository files = files committed under folders like scenarios/cso/current/
Release asset = the ZIP file attached to a GitHub Release for easy downloading
```

GitHub does **not** automatically check that the attached ZIP file matches the tagged repository state.

Before publishing a release, make sure the ZIP packet was created from files that are already committed in the relevant `current/` folder.

The rule is:

```text
Commit first. Release second.
```

Do not create a release ZIP from files on your desktop unless those same files have already been uploaded and committed to the repository.

## When to create a release

Create a release when we need a stable, citable, downloadable package.

Good reasons include:

- A specific workshop or training event
- A pilot or demo
- A partner handoff
- A translation milestone
- A major scenario revision
- A public distribution package

Do not create a release for every small edit.

## Release and tag naming

Use clear names that describe the scenario and purpose.

For event-specific releases, prefer names like:

```text
{scenario}-{date-or-event}
```

Examples:

```text
cso-2026-07-workshop
campaign-pilot-2026-09
observers-regional-training-2026-10
```

For milestone releases, use:

```text
{scenario}-v{major}.{minor}
```

Examples:

```text
cso-v1.0
campaign-v1.2
parliament-fr-v1.0
```

The tag name and release name do not have to be identical, but they should clearly match.

Example:

```text
Tag: cso-2026-07-workshop
Release title: CSO July 2026 Workshop Resource Packet
```

Avoid vague tag names like:

```text
final
latest
updated-files
july-stuff
```

## File naming convention

Use stable PDF filenames:

```text
cybersim-{scenario}-{language}-{type}.pdf
```

Examples:

```text
cybersim-cso-en-facilitator-guide.pdf
cybersim-cso-en-role-cards.pdf
cybersim-cso-en-table-tents.pdf
cybersim-cso-en-scenario-cards.pdf
cybersim-campaign-en-facilitator-guide.pdf
cybersim-parliament-fr-scenario-cards.pdf
```

Suggested scenario codes:

```text
campaign
cso
parliament
observers
```

Suggested language codes use ISO 639-1 two-letter codes:

```text
en
fr
es
ar
```

## ZIP packet naming convention

Each release should attach one ZIP file.

Use a clear ZIP filename:

```text
cybersim-{scenario}-{language}-resource-packet-{date-or-version}.zip
```

Examples:

```text
cybersim-cso-en-resource-packet-2026-07-workshop.zip
cybersim-cso-en-resource-packet-v1.0.zip
cybersim-campaign-en-resource-packet-pilot-2026-09.zip
cybersim-parliament-fr-resource-packet-v1.0.zip
```

## What to include in the ZIP packet

The ZIP file should contain the PDFs and other ready-to-use resources needed for that event or milestone.

Example ZIP contents:

```text
cybersim-cso-en-facilitator-guide.pdf
cybersim-cso-en-role-cards.pdf
cybersim-cso-en-table-tents.pdf
cybersim-cso-en-scenario-cards.pdf
```

Do not include editable source files in the release ZIP unless there is a specific reason to distribute them.

The release ZIP is meant to be the easy download packet for facilitators, printers, or partners.

## How to make a ZIP file

First, gather the committed files you want to include.

A simple approach:

1. Download or copy the files from the scenario’s `current/` folder.
2. Put them in a normal folder on your computer.
3. Name the folder something clear, such as:

```text
cybersim-cso-en-resource-packet-2026-07-workshop
```

4. Compress that folder into a ZIP file.

On macOS:

1. Right-click or Control-click the folder.
2. Choose **Compress “[folder name]”**.
3. macOS will create a `.zip` file next to the folder.

On Windows:

1. Right-click the folder.
2. Choose **Send to** → **Compressed (zipped) folder**.
3. Windows will create a `.zip` file.

The ZIP filename should be clear before you attach it to the release.

## How to publish a release

1. Make sure the correct files are already committed in the scenario’s `current/` folder.
2. Download or gather those committed files on your computer.
3. Put the files into a clearly named folder.
4. Compress that folder into a ZIP file.
5. Go to the repository on GitHub.
6. Click **Releases**.
7. Click **Draft a new release**.
8. Create a new tag, such as `cso-2026-07-workshop` or `cso-v1.1`.
9. Add a release title.
10. Write brief notes explaining what the release is for.
11. Attach the ZIP packet.
12. Click **Publish release**.

Example: for a CSO workshop, use the current CSO files from `scenarios/cso/current/`, put them into a folder called `cybersim-cso-en-resource-packet-2026-07-workshop`, compress that folder into a ZIP file, and attach the ZIP file to the release.

## Suggested release notes format

```markdown
## Purpose

Resource packet for the CSO scenario workshop in July 2026.

## Includes

- Facilitator guide
- Role cards
- Table tents
- Scenario cards

## Scenario

- Scenario: CSO
- Language: English
- Intended use: In-person facilitated session

## Repository snapshot

This release is attached to the tag `cso-2026-07-workshop`, which marks the state of the repository when this packet was created.

## Attached packet

- `cybersim-cso-en-resource-packet-2026-07-workshop.zip`

## Notes

- Files are based on the current resources in `scenarios/cso/current/`.
- This release is a frozen event packet and may not match later updates on `main`.
- Other scenario folders may exist in the repository but are not part of this release packet.
```

## Linking to files

For normal current files, link to the files in the repository’s `current/` folders.

For frozen event or milestone packets, link to the GitHub Release.

Avoid relying on `releases/latest` links unless we intentionally decide that a website should always point to the newest published release. In this repository, `current/` is the normal home for the latest approved files.

## Core rule

Use `current/` for the latest printable and ready-to-use files.

Use Releases only when we need to freeze a specific ZIP resource packet.
