# Output Review

## Objective

Inspect AI-produced output before accepting, sharing, merging, or acting on it.

## Resources And Materials

- The generated PR title and summary
- The PR for the endpoint change
- Copilot PR review comments
- The Copilot-created PR from the GitHub Actions segment
- Access to the actual diff and issue text for comparison

## Facilitator Actions

### Review The PR Title And Summary

1. Compare the generated title to the actual change.
2. Compare the summary to the diff, not to your intent alone.
3. Edit or reject any wording that overstates the change or invents rationale.

### Gate 5: PR Review Handoff

1. Assign Copilot to review the endpoint PR.
2. Capture the feedback Copilot provides.
3. Remind participants that this is the Gate 5 checkpoint for the first segment: the PR is now entering the normal review path.
4. Confirm that Copilot feedback is advisory and that a human still owns the decision.

### Review Copilot PR Comments

1. Read each comment against the actual code.
2. Classify it as one of the following:

Classification options:

- valid and actionable
- partially useful but needs human interpretation
- incorrect or out of scope

1. Explain why you are keeping or discarding the comment.

### Review The Cloud-Agent PR

1. Read the PR description and changed files.
2. Verify the implementation matches the issue scope.
3. Look for assumptions the agent made without support from the issue.
4. Confirm no unrelated files or workflow changes were introduced.
5. Confirm the PR is still focused on the breed-filter feature request.

## Phase Gate Checkpoint

Implement Gate 4 after every generated output. For the endpoint PR, follow Gate 4 immediately with Gate 5 by assigning Copilot as reviewer and treating that as the review handoff checkpoint.

Gate 4 questions:

- Does the output match the requested scope?
- Were unsupported claims or invented details removed?
- Did the output avoid secrets or sensitive information?
- Can the human reviewer explain the result?
- Are the next validation steps clear?

Gate 5 handoff questions for the PR demo:

- Has the PR been handed into the normal review process?
- Has Copilot review feedback been captured and inspected?
- Is it clear that human reviewers still approve, reject, or revise the change?

If the reviewer cannot explain the output, do not keep it.

## Key Points To Emphasize

- Good-looking output is still draft until reviewed.
- Human review is about correctness, scope control, and accountability.
- The first segment ends with PR review handoff, not merge.
- PR review assistance and cloud-agent output both require the same review discipline, even though the surface is different.
