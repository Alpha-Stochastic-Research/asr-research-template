# New Project Setup

After creating a repository from this template, complete the following checklist.

## General Information

* [ ] Replace the title in `README.md`.
* [ ] Add a clear project description.
* [ ] Add the research topic and objectives.
* [ ] Add the project leads or maintainers.
* [ ] Define the project status: experimental, active, maintained, or archived.

## Python Metadata

In `pyproject.toml`:

* [ ] Replace `asr-project` with the actual package name.
* [ ] Update the project description.
* [ ] Verify the required Python version.
* [ ] Add the required dependencies.

## Citation

In `CITATION.cff`:

* [ ] Replace `ASR Project` with the actual project title.
* [ ] Verify the authors.
* [ ] Verify the version.
* [ ] Verify the license.
* [ ] Replace `REPOSITORY` with the actual repository name.

## Security

* [ ] Never commit a `.env` file.
* [ ] Never commit API keys, passwords, or credentials.
* [ ] Verify that `CODEOWNERS` references `release-admins`.
* [ ] Verify that Pull Requests are enabled.
* [ ] Verify that the organization ruleset applies to the repository.

## Quality

* [ ] Run `ruff check .`.
* [ ] Run `pytest`.
* [ ] Verify that the GitHub Actions CI workflow passes.
* [ ] Document the data sources and data provenance.
* [ ] Document the scientific or technical limitations.

Once this checklist has been completed, it may be deleted through an approved Pull Request.
