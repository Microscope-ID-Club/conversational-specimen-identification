# Conversational specimen identification

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23531039.svg)](https://doi.org/10.5281/zenodo.23531039)

This repository presents a conversational method for examining, describing, and identifying biological specimens with an AI companion. It is designed for naturalists and ecologists. No knowledge of R is required.

The method does not treat identification as a race through a key. It begins with the intact specimen, gathers observations in convenient groups, organises them into a biological hierarchy, and only then tests identification hypotheses against keys and reference descriptions.

This is a method and feasibility resource. It does not claim that AI can determine specimens reliably from images, replace taxonomic expertise, or provide validation across taxa. Determinations still depend on observer-made examination, adequate evidence, suitable identification resources, and expert review where appropriate.

## What this repository provides

- `AGENTS.md` gives an AI coding companion detailed instructions for guiding specimen examination and identification.
- `METHOD.md` explains the reasoning behind the method.
- `RECORD_FORMAT.md` defines a stable, portable Markdown record format.
- `templates/specimen-record.md` is a neutral starting point for a specimen record.
- `examples/example-specimen.md` demonstrates the format using fictional observations.
- `records/` explains how records may be organised, but is not intended to hold project data in this public repository.

The instructions between the marker comments in `AGENTS.md` are synchronised from a canonical copy maintained in `eco.records`. That package is currently private development software and is not presented as a CRAN-ready release. Access may be made available on request, but the package is not required to use this method or contribute suggestions. Repository-specific instructions follow the managed section.

## Start a project from the template

For a new site-based, organisational, or personal trial, use the separate [specimen-identification project template](https://github.com/Microscope-ID-Club/specimen-identification-project-template). It provides project-scope and governance placeholders while keeping this DOI-bearing repository as the stable, citable source of the method.

Repositories created from the template are independent copies and do not receive later changes automatically. Their project owners remain responsible for checking the source method, reviewing local instructions, and deciding access and reuse terms for specimen records and images.

## Recommended: use the repository

1. Create a repository for your project with **Use this template** in the [specimen-identification project template](https://github.com/Microscope-ID-Club/specimen-identification-project-template). If that is not practical, clone or download the template repository, or copy its files into a project folder that you control.
2. Create a folder for the specimen using a stable identifier, for example `SPECIMEN-001`.
3. Copy `templates/specimen-record.md` into that folder and rename the copy `record.md`.
4. Replace the example record identifier in both the metadata and title.
5. Add an `images/` subfolder if supporting photographs are available.
6. Open this repository as the primary local project in Codex.
7. Start a new chat and say: `Guide me through examining and identifying specimen SPECIMEN-001 according to the project instructions.`
8. Describe what you observe. Do not begin by asking for image matching or by treating a tentative name as established.
9. Review the evolving `record.md` in RStudio. Correct anything that does not accurately represent the observation.

Before working with real records, decide separately where they should be stored, who may access them, and whether locality, personal, third-party, or other sensitive information needs to be withheld or generalised. This public repository should contain only fictional or suitably generalised examples.

## Use the method without Git or a repository

Git is recommended because it preserves revision history and makes the method, records, and proposed improvements easier to manage. It is not a requirement.

If you cannot clone or manage a repository:

1. Open `AGENTS.md` and copy its contents into the instructions or opening message of a conversational AI system that accepts user-supplied instructions.
2. Explain that you want to examine a specimen using those instructions.
3. Describe your observations in the conversation. The AI should guide the examination even when it cannot create or edit files.
4. Ask the AI to maintain a portable Markdown record in the conversation, using `templates/specimen-record.md` if you can also supply that file.
5. Periodically copy the record into a document or plain-text file that you control. Review it carefully and correct anything that does not accurately represent your observations.

If you cannot supply the template, the instructions still apply. The AI can keep a simpler structured account in the conversation and provide a copyable summary. Availability and behaviour vary between AI systems, so retain your own copy rather than relying on the conversation as the only durable record.

## Editing in RStudio

Open `conversational-specimen-identification.Rproj`, then select a Markdown file from the Files pane. The files are ordinary text. The main Markdown conventions used here are:

- `#`, `##`, and `###` introduce headings;
- `-` introduces a list item;
- indentation creates a nested list;
- blank lines separate paragraphs and lists.

No R code or package installation is required.

## Contributing

Suggestions, corrections, and proposed improvements are welcome through GitHub issues and pull requests. See `CONTRIBUTING.md`, particularly before changing the managed section of `AGENTS.md`.

## Project trials

This general repository is deliberately separate from any site-based or organisational trial. A trial should use its own repository for participant instructions, permissions, governance, records, and images while retaining or synchronising the general method as appropriate.

## Licence

Except where otherwise stated, the repository materials are licensed under the Creative Commons Attribution 4.0 International licence (`CC BY 4.0`). See `LICENSE.md`.

## AI use and responsibility

Generative AI tools assisted the development and revision of these materials and are also the subject of the method described here. Paul J. Palmer directed the work, reviewed the repository contents, and accepts responsibility for them. AI tools are not authors or creators of this resource. No AI-generated observation, image, measurement, reference, or identification should be presented as empirical evidence.

The method and record format remain under development. The `format_version` in each record allows the structure to evolve while supporting deliberate migration into other recording systems.
