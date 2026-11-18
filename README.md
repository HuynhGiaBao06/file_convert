# DocConvert

DocConvert is a planned Python toolkit for document extraction and composition, with an object-oriented application layer and a CLI.

## Current state

The workspace currently contains the legacy image-to-PDF scripts. The new package and CLI are planned. Conversion quality and runtime behavior have not been revalidated during the documentation setup.

## Existing usage

Install dependencies with `python -m pip install -r requirements.txt`.
Place images in a subdirectory of `data/`, then run:

```powershell
python path.py --folder Chapter_1 --per-page 1 --fit contain
python path.py --help
```

The script writes PDFs to `report/`. It accepts image directories and ZIP archives. Supported image extensions are PNG, JPG, JPEG and WEBP. Existing output files can be replaced.

## Target capabilities

| Operation | Inputs | Output | State |
| --- | --- | --- | --- |
| compose | Images, image directories, ZIP | PDF | Planned rewrite |
| extract | PPTX | Markdown and assets | Planned first extraction route |
| extract | PDF and images | Markdown and assets | Planned subsequent routes |
| transcode | Selected format pairs | Layout-oriented conversion | Future extension |

The proposed CLI uses `docconvert compose` and `docconvert extract`. These commands become usable after package implementation and installation.

## Project guidance

- [Architecture](docs/architecture.md) defines module boundaries and acceptance criteria.
- [Agent instructions](AGENTS.md) define scope and evidence rules.
- [Working procedure](.agent/workflow.md) defines task handoff and selective context loading.
- [Task template](.agent/templates/task.md) captures the task contract.
- [Handoff template](.agent/templates/handoff.md) captures a resumable checkpoint.

Project documentation, templates, checkpoints and skill instructions use English. Conversation language follows the user.

## Implementation sequence

1. Establish documentation and agent guidance.
2. User creates and connects the Git repository.
3. Implement package foundations and typed application contracts.
4. Implement image composition and PPTX extraction as separate work items.
5. Add PDF and image extraction after fixture-based evaluation.
6. Add optional providers or direct conversion routes when required.

Git repository creation and remote connection are performed by the user.
