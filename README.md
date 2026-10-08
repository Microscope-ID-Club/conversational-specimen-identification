# Specimen identification trial

This private pilot tests a conversational method for examining, describing, and identifying biological specimens. It is designed for naturalists and ecologists. No knowledge of R is required.

The method does not treat identification as a race through a key. It begins with the intact specimen, gathers observations in convenient groups, organises them into a biological hierarchy, and only then tests identification hypotheses against keys and reference descriptions.

## Trial scope

The initial trial is limited to specimens from Rutland Water Nature Reserve (RWNR). RWNR specimen and locality information may be recorded under the reserve's policy of publicising discoveries and managing access positively.

Do not add:

- specimens from outside RWNR unless permission is confirmed or the locality is generalised;
- passwords, access credentials, private contact details, confidential correspondence, or security arrangements;
- third-party records that you do not have permission to use.

## Repository contents

- `AGENTS.md` tells Codex how to guide the examination and identification.
- `METHOD.md` explains the reasoning behind the method.
- `RECORD_FORMAT.md` defines the stable Markdown format used by future importers.
- `templates/specimen-record.md` is copied for each new specimen.
- `examples/example-specimen.md` demonstrates the format using fictional observations.
- `records/` contains one folder per trial specimen.

## Start a specimen record

1. Create a folder under `records/` using a stable identifier, for example `BETH-2026-001`.
2. Copy `templates/specimen-record.md` into that folder and rename the copy `record.md`.
3. Replace the example record identifier in both the metadata and title.
4. Add an `images/` subfolder if supporting photographs are available.
5. Open this repository as the primary local project in Codex.
6. Start a new chat and say: `Guide me through examining and identifying specimen BETH-2026-001 according to the project instructions.`
7. Describe what you observe. Do not begin by asking for image matching or by treating a tentative name as established.
8. Review the evolving `record.md` in RStudio. Correct anything that does not accurately represent the observation.

## Editing in RStudio

Open `specimen-identification-trial.Rproj`, then select a Markdown file from the Files pane. The files are ordinary text. The main Markdown conventions used here are:

- `#`, `##`, and `###` introduce headings;
- `-` introduces a list item;
- indentation creates a nested list;
- blank lines separate paragraphs and lists.

No R code or package installation is required.

## Git workflow for the pilot

Keep the first trial simple:

1. Pull or synchronise before starting work.
2. Review the changed files.
3. Commit with a short message such as `Add initial observations for BETH-2026-001`.
4. Push or synchronise the commit to the private GitHub repository.

Ask for help rather than resolving a Git conflict by deleting or overwriting a record.

## Status

This is a pilot format. The `format_version` in each record allows the structure to evolve while supporting import into other recording systems.
