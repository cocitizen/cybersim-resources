# CyberSim Resources

Printable and editable resources for running CyberSim scenarios.

This repository stores facilitator guides, role cards, scenario cards, table tents, handouts, design source files, and other materials used to run CyberSim in person.

The goal is simple: keep one clear current version of each resource, keep editable source files nearby, and preserve history without making documents behave like software code.

## What’s in here

Materials are organized by scenario.

Each scenario may include:

- **Current PDFs** — the latest approved files to print or share
- **Source files** — editable originals, such as InDesign files, IDML files, linked images, and templates
- **Archive files** — old or retired files that should not be used for current sessions

Recommended structure:

```text
scenarios/
  cso/
    README.md
    current/
    source/
    _archive/

  campaign/
    README.md
    current/
    source/
    _archive/

shared/
  logos/
  templates/
  icons/
```

## How to use this repository

Use the files in a scenario’s `current/` folder when printing or sharing materials.

For example:

```text
scenarios/cso/current/
```

should contain the latest approved PDFs for the CSO scenario.

If someone is running a CyberSim session tomorrow, `current/` should be the first place they look.

## Editing and exporting

To update a resource:

1. Edit the matching file in `source/`.
2. Export a new PDF.
3. Replace the matching PDF in `current/`.
4. Upload the updated source file and exported PDF.
5. Commit the change with a short plain-English note describing what changed.

Example commit messages:

```text
Update CSO role cards with revised team names
```

```text
Fix typo in facilitator guide and re-export PDF
```

```text
Replace table tents with print-ready version for July workshop
```

## File naming

Keep filenames stable.

Use names like:

```text
cybersim-cso-en-facilitator-guide.pdf
cybersim-cso-en-role-cards.pdf
cybersim-cso-en-table-tents.pdf
cybersim-cso-en-scenario-cards.pdf
```

Avoid names like:

```text
role-cards-final.pdf
role-cards-final-v2.pdf
role-cards-use-this-one.pdf
```

When updating a PDF, replace the existing file with the same name. GitHub keeps the file history.

## Source files

Editable originals should live in `source/`.

For InDesign materials, include the files needed to reopen and edit the document later, such as:

- `.indd`
- `.idml`
- linked images
- packaged assets
- short notes if special fonts, exports, or print settings are required

Do not edit PDFs directly unless there is no source file available.

## Archive files

The `_archive/` folder is for old files that should not be used for current sessions.

GitHub already keeps version history, so `_archive/` should be used sparingly. It is mainly a practical holding place for retired materials that people may not want to delete yet.

## Repository hygiene

This repository should contain the files needed to edit, export, print, share, or understand CyberSim resources.

Please avoid committing files that are not needed, such as temporary exports, duplicate drafts, local backup files, cache files, or “just in case” copies.

Before adding a file, ask:

- Is this needed to edit the resource later?
- Is this the current exported file people should use?
- Is this a shared asset, template, or note that helps explain the resource?
- Is this an intentionally archived file that should no longer be used?

If the answer is no, it probably does not belong in the repository.

Keep filenames clear and stable. Avoid files named `final`, `final-v2`, `new`, `old`, `copy`, or `use-this-one`.

Use `_archive/` sparingly for retired materials that should not be used for current sessions. GitHub already preserves file history, so old versions usually do not need to be kept as separate files.

## Releases

GitHub Releases are optional and should be used only when we need to freeze the exact files used for a specific event, workshop, pilot, translation milestone, or public release.

For everyday work, the current printable files live in each scenario’s `current/` folder.

See [RELEASES.md](RELEASES.md) for the release workflow.