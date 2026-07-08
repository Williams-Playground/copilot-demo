# GitHub Issue And Actions Demo

## Objective

Show the second and third demo segments: a GitHub issue assigned to Copilot, followed by a PR comment that triggers the repository workflow.

## Resources And Materials

- Local app or test environment
- The PR opened from the GitHub Actions segment
- The workflow file at `./.github/workflows/codeowner-update.lock.yml`
- Repository checks, workflow status, and code-owner review status

## Facilitator Actions

### 1. Run The GitHub Issue Demo

1. Confirm the `COPILOT_GITHUB_TOKEN` secret is configured.
2. Create a new issue for the feature request below.
3. Assign Copilot to the issue so it opens a PR.
4. When the PR opens, review it for scope, assumptions, and changed files.

Feature request text:

The website currently lists all dogs in the database. While this was appropriate when the shelter only had a few dogs, as time has gone on the number has grown and it's difficult for people to sift through who's available to adopt. The shelter has asked you to add filters to the website to allow a user to select a breed of dog and only display dogs which are available for adoption.

### 2. Review The Issue PR Output

1. Confirm the Copilot-created PR is still within issue scope.
2. Verify the PR is actually implementing the breed-filter feature and not just backend scaffolding.
3. Review repository checks, comments, and approvals through the normal PR flow.
4. Confirm a human remains accountable for merge or release.

### 3. Run The GitHub Actions Demo

1. Add the agreed trigger comment to the issue-generated PR.
2. Explain that the comment is intended to trigger `./.github/workflows/codeowner-update.lock.yml`.
3. Watch the workflow run and confirm it is the expected automation path.

### 4. Perform Security And Data Review

1. Confirm no secrets, tokens, or sensitive content were added to the PR, issue, or summary.
2. Call out any auth, dependency, or configuration changes for explicit human review.
3. Reiterate that the token was required because the later hosted and workflow segments depend on it.

### 5. Close With Handoff

1. State what is ready for normal review.
2. State what still requires human approval.
3. Route the work through the standard repository process.

### 6. Capture Lessons Learned

At the end of the demo, record:

- what prompt or issue format worked well
- what review issue the audience caught
- what guardrail should be reused next time

## Phase Gate Checkpoint

Implement Gate 5 at the end of the issue and workflow segments, before any merge, approval, or external sharing.

Gate 5 questions:

- Was validation completed at the right level for the change?
- Was security or data review completed where needed?
- Did the work go through the normal source-control path?
- Is human accountability visible?
- Was a reusable lesson captured?

## Key Points To Emphasize

- Validation is where the demo proves that AI assistance did not bypass engineering controls.
- The second and third segments show that hosted Copilot work and repository automation still return to the same human-owned review path.
- The workflow is only successful if human review, repository approval, and release ownership remain intact.
- End by showing that the process is repeatable because the gates are explicit.
