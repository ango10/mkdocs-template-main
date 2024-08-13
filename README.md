# mkdocs-template

Use this template as a starting point for setting up a docs-as-code workflows in your project repository.

This template uses the Backstage [`mkdocs-techdocs-core`](https://github.com/backstage/mkdocs-techdocs-core) plugin, so the documentation can easily be integrated into Backstage.io.

This repository borrows templates for conceptual docs, how-to guides, and contributiing guides from [The Good Docs Project](https://thegooddocsproject.dev/). For more templates, visit the [Good Docs Project / Templates repository on GitLab](https://gitlab.com/tgdp/templates/-/tree/main?ref_type=heads).

## Preview the site locally

On a machine with Python installed:

1. Clone this repository.
2. Install [MkDocs](https://www.mkdocs.org/)

    ```console
    pip install mkdocs
    ```

3. Install the mkdocs-techdocs-core plugin.

    ```console
    pip install mkdocs-techdocs-core
    ```

4. Navigate to the root of the template repo and run `mkdocs serve`.

    ```console
    cd mkdocs-template
    mkdocs serve
    ```

5. Open up [http://127.0.0.1:8000/](http://127.0.0.1:8000/) in your browser.

## Add pages

See [MkDocs - Writing your docs](https://www.mkdocs.org/user-guide/writing-your-docs).

## Change the navigation

See [Mkdocs - Configure Pages and Navigation](https://www.mkdocs.org/user-guide/writing-your-docs/#file-layout).

## Demo

This repo uses a [GitHub action](https://github.com/StrategicProductDevelopment/mkdocs-template/blob/main/.github/workflows/main.yml) that triggers on each merge against the `main` branch to:

1. Install MkDocs and plugins.
2. Build a new version of the docs site from files in the `docs` directory.
3. Commit the site to the [`gh-pages`](https://github.com/StrategicProductDevelopment/mkdocs-template/tree/gh-pages) branch.

The `gh-pages` branch is hosted as a GitHub pages site at [fictional-adventure-wo1w7r1.pages.github.io](https://fictional-adventure-wo1w7r1.pages.github.io/)

## Minimum viable docs

This table provides recommendations on what to include when using this template to set up your own docs site:

| Page                                      | Path                                | Description                                                                                          | Req/Opt           |
| ----------------------------------------- | ----------------------------------- | ---------------------------------------------------------------------------------------------------- | ----------------- |
| Home                                      | `docs/index.md`                     | Home page                                                                                            | Required          |
| API > Overview                            | `docs/api/overview.md`              | API overview                                                                                         | Required for APIs |
| API > Quickstart                          | `docs/api/quickstart.md`            | Quickstart + authentication info                                                                     | Optional          |
| SDK > {Library} SDK                       | `docs/sdk/index.md`                 | Details about a given SDK. Create multiple for products with multiple libraries.                     | Required          |
| Architecture                              | `docs/architecture.md`              | System architecture + diagrams                                                                       | Optional          |
| {Business process} > About {concept name} | `docs/<business-process-name>/*.md` | Template for conceptual docs for a given feature/business process/capability.                        | Varies by product |
| Business process > How to {task name}     | `docs/<business-process-name>/*.md` | Template for how-to guide for a given feature/business process/capability. Create as many as needed. | Varies by product |
| Glossary                                  | `docs/glossary.md`                  | Glossary of terms and acronyms                                                                       | Optional          |
| Release Notes                             | `docs/release-notes.md`             | Release notes                                                                                        | Required          |
| Contributing                              | `docs/contributing.md`              | How to contribute to the project                                                                     | Required          |