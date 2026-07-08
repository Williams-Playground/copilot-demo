# Context Approval

## Objective

Approve the minimum context needed for the next AI action and exclude anything unrelated, sensitive, or unnecessary.

## Resources And Materials

- The prepared code diff for the PR review segment
- The issue text for the GitHub Actions segment
- The trigger comment that will be added to the issue-generated PR
- The specific files or excerpts needed to explain the task

## Facilitator Actions

### For The PR Review Segment

1. Show only the pull request diff or the specific changed files.
2. Share the problem statement in one or two sentences.
3. Avoid opening unrelated folders or pasting broad repository context.

### For The GitHub Actions Segment

1. Write the issue so the goal, constraints, and acceptance criteria are explicit.
2. Include only the repository area needed for the task.
3. Remove or avoid secrets, environment details, and unrelated backlog context.

### For The Workflow Trigger Segment

1. Show the exact trigger comment that will be posted to the PR.
2. Reference the workflow file `./.github/workflows/codeowner-update.lock.yml` so participants know what automation is being exercised.
3. Avoid adding unrelated commands or comments that could confuse the trigger path.

## Phase Gate Checkpoint

Implement Gate 2 immediately after selecting the files, diff, or issue text and before running Copilot.

Gate 2 questions:

- Is the selected context approved for this tool surface?
- Has sensitive information been removed or avoided?
- Is the context limited to what the task actually needs?
- Does the repository or artifact owner agree with this use pattern?
- Is the audience clear on whether the workflow is local or hosted?

If the context is broader than needed, reduce it before continuing.

## What Good Context Looks Like

### Good For PR Review

- one small diff
- one PR description
- one clearly stated goal

### Good For GitHub Actions

- one bounded issue
- explicit acceptance criteria
- one target area of the repo

### Good For The Workflow Trigger

- one exact PR comment
- one referenced workflow file
- one expected automation outcome

### Poor Context

- the whole repository with no task boundary
- screenshots or notes that include unrelated customer data
- vague issue text that forces the agent to invent missing requirements
- multiple trigger comments with no clear explanation of which workflow they invoke

## Key Points To Emphasize

- More context is not automatically better.
- Context approval is where data minimization happens.
- Local and hosted workflows may have different risk profiles; call that out before moving on.
