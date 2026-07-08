# Prompt Or Run Approval

## Objective

Approve the exact AI action before you invoke it. The request should be bounded, reviewable, and explicit about what must not be guessed.

## Resources And Materials

- Approved diff or issue text from the previous step
- A prepared stop condition statement
- Validation steps appropriate to the task

## PR Demo Segment

### Step 1: Open The Pull Request

1. Implement the narrow backend endpoint from intake.
2. Create or open a pull request for that small change.
3. Confirm the diff is still small enough for a live review.

Gate note:

- This is the last point to shrink scope before asking Copilot to generate anything.

### Step 2: Generate Title And Summary

1. Ask Copilot to generate the PR title and summary.
2. Keep the request narrow: summarize only what changed and why.

Implement Gate 3 immediately before triggering generation.

### Step 3: Prepare For Output Review

1. Pause before requesting any review feedback.
2. Move to the output review step so the generated PR text can be inspected first.

## GitHub Issue Segment

### Step 1: Create The Issue

1. Create a new issue with one clear change request.
2. Use the breed-filter feature description from intake.
3. Include acceptance criteria and any explicit constraints.

### Step 2: Assign Copilot To The Issue

1. Confirm the issue is still bounded and testable.
2. Assign Copilot to the issue so it opens a PR.

Implement Gate 3 immediately before assigning the issue.

### Step 3: Trigger The Follow-On Review Workflow

1. When the PR opens, inspect the title and scope before doing anything else.
2. Do not trigger the workflow yet. Save that for the final GitHub Actions segment.

## GitHub Actions Segment

### Step 1: Trigger The Workflow

1. Confirm the issue-generated PR is the correct target.
2. Add the trigger comment to the PR.
3. State that this comment is intended to exercise `./.github/workflows/codeowner-update.lock.yml`.

## Phase Gate Checkpoint

Gate 3 questions:

- Is the goal stated clearly?
- Are the constraints and expected output form explicit?
- Did we tell the tool not to invent missing facts or rules?
- Are validation steps named?
- Are stop conditions clear if the result drifts or expands?
- Are the allowed actions and tools understood?

## Example Guardrail Language

Use language like this before the run:

```text
Use only the approved context for this task.
If information is missing, list it instead of guessing.
Keep the output small and reviewable.
Do not make release, security, or business-rule decisions.
Return output as draft for human review.
```

## Stop Conditions To Call Out Live

Stop and return to human review if:

- the task expands beyond the agreed scope
- the output proposes architecture changes that were not requested
- the agent needs broader context than was approved
- the result touches secrets, auth, or security-sensitive paths unexpectedly

## Key Points To Emphasize

- Approval is not just permission to click a button; it is where you define the safe boundary of the run.
- Repeat Gate 3 before each distinct AI action, not just once at the start of the demo.
