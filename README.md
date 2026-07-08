# GitHub PR Reviews and GitHub Actions

This repository contains the project for three guided workshops to explore various GitHub features. The project is a website for a fictional dog shelter, with a [Flask](https://flask.palletsprojects.com/en/stable/) backend using [SQLAlchemy](https://www.sqlalchemy.org/) and an [Astro](https://astro.build/) frontend using [Tailwind CSS](https://tailwindcss.com/).

## Source repos
- https://github.com/github-samples/pets-workshop.git (For the demo application and some test scenarios)
- https://github.com/github/awesome-copilot (The the demo github workflow)

## What This Demo Is Trying To Achieve

This demo is designed to show how GitHub Copilot can be used inside a human-in-the-loop workflow without bypassing review, approval, or repository controls. The goal is not just to show Copilot generating output, but to show where humans deliberately pause, approve context, review results, and hand work back into the normal pull request process.

The demo is split into three segments:

1. A small endpoint change is implemented and opened as a pull request. Copilot is used to generate the PR title and summary, and the PR then moves into a normal review handoff.
2. A new feature request is created as a GitHub issue and assigned to Copilot, which opens a PR for the feature. That PR is then reviewed for scope, correctness, and assumptions.
3. A comment is added to the issue-generated PR to trigger the repository workflow at [codeowner-update.lock.yml](./.github/workflows/codeowner-update.lock.yml), showing that automation still runs inside the expected repository approval path.

Across all three segments, the demo highlights the phase gates from the human-in-the-loop agenda: intake, context approval, prompt or run approval, output review, and final handoff through normal PR and workflow review.

The detailed walkthrough for the demo lives in the [demo](./demo) folder.

## Getting started

> **[Get started learning about development with GitHub!](./content/README.md)**

## License

This project is licensed under the terms of the MIT open source license. Please refer to the [LICENSE](./LICENSE) for the full terms.

## Maintainers

You can find the list of maintainers in [CODEOWNERS](./.github/CODEOWNERS).

## Support

This project is provided as-is, and may be updated over time. If you have questions, please open an issue.
