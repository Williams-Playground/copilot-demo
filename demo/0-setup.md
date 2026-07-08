# Setup

## Objective

Prepare the environment, credentials, and demo artifacts before starting the live walkthrough.

## Prerequisites

- Python 3 for the Flask backend
- Node.js and npm for the Astro client
- VS Code with the GitHub Copilot extension
- A GitHub account with Copilot access
- Access to the demo repository with permission to create issues, open pull requests, comment on pull requests, and manage Actions secrets

## Resources And Materials

- GitHub access to the target repository with permission to manage secrets, create issues, and open pull requests
- Local clone of this repo
- Node.js and npm installed locally so the Astro client can start
- A terminal window and browser window ready for screen share
- A small, reviewable code change prepared for the PR review segment
- A sample issue statement for the GitHub Actions segment
- Access to the workflow file at `./.github/workflows/codeowner-update.lock.yml`

## 1. Create The Copilot Token

Open [Create a fine-grained PAT](https://github.com/settings/personal-access-tokens/new?name=COPILOT_GITHUB_TOKEN&description=GitHub+Agentic+Workflows+-+Copilot+engine+authentication&user_copilot_requests=read) and verify the following before generating it:

1. Resource owner is your user account, not an organization.
2. Under Permissions, Account permissions, `Copilot Requests` is set to `Read`.
3. Generate the token and copy the value once.
4. Add it to the repository under Settings, Secrets and variables, Actions as `COPILOT_GITHUB_TOKEN`.

Why this matters for the demo:

- the token is required for the hosted Copilot issue-assignment flow
- the final GitHub Actions segment uses the PR comment trigger path tied to the codeowner workflow

## 2. Start The App

Run one of the following commands from the repository root:

- macOS or Linux: `./app/scripts/start-app.sh`
- Windows PowerShell: `./app/scripts/start-app.ps1`

## 3. Validate The App Is Reachable

Use a browser to confirm both application surfaces respond:

- `http://localhost:5100/api/dogs`
- `http://localhost:4321`

If either page does not load, stop here and fix the environment before the demo begins.

## 4. Prepare The Demo Surfaces

Before starting the live demo, have these ready:

1. A feature branch with a small code change that is safe to review in one sitting.
2. The repository Actions secret page, in case you need to confirm `COPILOT_GITHUB_TOKEN`.
3. A draft issue for the cloud-agent workflow. Keep it small, explicit, and testable.
4. The demo files in this folder open in the editor for quick navigation.
5. The workflow file `./.github/workflows/codeowner-update.lock.yml` open and ready to reference during the final segment.

## Key Points To Emphasize

- Setup is not a gate by itself. It is preparation for the formal human-in-the-loop checkpoints that begin in the intake step.
- Keep the change and the issue intentionally small. The demo works better when the audience can read the entire scope quickly.
- Call out early that the token is needed because the later issue-assignment and workflow-trigger steps depend on hosted Copilot and repository automation.
- Do not use production data, private credentials, or unrelated repository context during the walkthrough.
