# Human-In-The-Loop Demo Agenda

Use the demo files in order. The flow is split into three live demo segments after setup and approvals.

## 1. Setup

Use [0-setup.md](./0-setup.md).

Outcome:

- local environment is running
- required GitHub secret is present
- facilitator has the demo materials ready
- the workflow trigger path is ready for the final segment

Gate note:

- setup is pre-work; formal phase gates begin in [1-intake.md](./1-intake.md)

## 2. Intake

Use [1-intake.md](./1-intake.md).

Outcome:

- participants agree the tasks are appropriate for AI assistance
- the endpoint PR, issue-assignment demo, and workflow-trigger demo are clearly separated
- owner, output, scope, and review boundaries are explicit

Gate checkpoint:

- Gate 1: Intake and suitability

## 3. Context Approval

Use [2-context.md](./2-context.md).

Outcome:

- only approved, minimal context is shared for each of the three demo segments

Gate checkpoint:

- Gate 2: Context approval

## 4. Demo Segment One: Endpoint PR

Use [3-run-approval.md](./3-run-approval.md).

Steps:

1. Implement the endpoint change introduced during intake.
2. Open a pull request for that small backend change.
3. Have Copilot generate the PR title and summary.

Gate checkpoint:

- Gate 3: Prompt or run approval before each Copilot action

## 5. Demo Segment One: Output Review And PR Review Handoff

Use [4-output-review.md](./4-output-review.md).

Steps:

1. Review the generated PR title and summary.
2. Compare the PR content to the actual endpoint change.
3. Assign Copilot to review the PR and capture the feedback.

Gate checkpoints:

- Gate 4: Output review
- Gate 5: PR review and handoff through the normal review process

## 6. Demo Segment Two: GitHub Issue Assigned To Copilot

Use [5-validation.md](./5-validation.md).

Steps:

1. Confirm the `COPILOT_GITHUB_TOKEN` secret is configured.
2. Create a bounded feature issue for breed-based dog filters.
3. Assign Copilot to the issue so it opens a PR.
4. Review the issue-generated PR for scope and correctness.

Gate checkpoints:

- Gate 3 before assigning Copilot to the issue
- Gate 4 when reviewing the generated PR output

## 7. Demo Segment Three: GitHub Actions Trigger

Use [5-validation.md](./5-validation.md).

Steps:

1. Add the agreed trigger comment to the issue-generated PR.
2. Show that [.github/workflows/codeowner-update.lock.yml](../.github/workflows/codeowner-update.lock.yml) is the workflow being exercised.
3. Confirm the comment-triggered workflow runs and returns control to the normal review path.

Gate checkpoints:

- Gate 3 before triggering the action with the comment
- Gate 5 when validating the workflow output and closing the demo
