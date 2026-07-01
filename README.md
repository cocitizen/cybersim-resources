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

## Releases

GitHub Releases are optional and should be used only when we need to freeze the exact files used for a specific event, workshop, pilot, translation milestone, or public release.

For everyday work, the current printable files live in each scenario’s `current/` folder.

See [RELEASES.md](RELEASES.md) for the release workflow.