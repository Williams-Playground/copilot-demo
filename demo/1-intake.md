# Intake

## Objective

Decide whether the work is appropriate for AI assistance before any prompt, review action, or cloud-agent run.

## Working Scenario For Discussion

Williams-Playground is a dog training and pet resort with a growing adoption program. William is meeting with the engineering team because staff are spending too much time answering basic navigation questions for visitors and internal users.

He starts with a narrow request: "Before we change the whole site, can we at least expose the list of breeds we already have?" That gives the team a small, reviewable first change.

Then he follows up with the broader request: "Next, I want adopters to filter the dogs they see so they do not have to scroll through everything." That becomes the separate issue used later in the demo.

For the first segment, keep the scope intentionally narrow:

- start with a backend endpoint that returns the available breeds
- defer the full filtering workflow until later

For the second segment, expand scope in a controlled way by using the breed-filter feature request as a separate issue rather than folding it into the first PR.

This is the right size for AI assistance because it is:

- owned by one stakeholder
- focused on one output slice
- narrow enough for a human to review quickly

## Demo Scenarios

### Scenario A: Endpoint Pull Request

Williams-Playground has grown over the last year. What started as a simple internal site for tracking dogs at the shelter is now used by more staff, more volunteers, and more adoption coordinators. William, one of the business stakeholders, has noticed that people keep asking the same question: "Can I just see the breeds we currently have?"

He is not asking for the full filtering feature yet. He wants the team to take one small step first: add a backend endpoint that returns the list of breeds already represented in the system. The team decides this is a good first slice because it is small, easy to explain, and easy to review. That small change becomes the first pull request in the demo.

Expected output:

- a small backend pull request for the endpoint change
- a generated PR title and summary
- Copilot review feedback during the PR handoff

### Scenario B: GitHub Issue Assigned To Copilot

Once the first pull request is understood, the conversation moves from "What breeds do we have?" to "How do we help adopters find the right dog faster?" The shelter staff explain that the website now lists every dog in one long page. That worked when the shelter only had a few dogs, but it has become harder for visitors to browse as the list has grown.

Instead of folding that larger change into the first pull request, the team captures it as a separate feature request. That issue is then assigned to Copilot so the audience can see how a bounded GitHub issue turns into a pull request, while humans still control the request, the scope, and the review.

Expected output:

- a clearly scoped issue
- a Copilot-created PR

Feature description for the issue:

The website currently lists all dogs in the database. While this was appropriate when the shelter only had a few dogs, as time has gone on the number has grown and it's difficult for people to sift through who's available to adopt. The shelter has asked you to add filters to the website to allow a user to select a breed of dog and only display dogs which are available for adoption.

### Scenario C: GitHub Actions Trigger

After the feature PR exists, the team wants to show one more step in the process: repository automation. A maintainer adds a comment to the PR, not as a magic shortcut, but as a deliberate trigger for a known workflow. This lets the audience see that automation still happens inside a controlled path, with named triggers, visible workflow files, and human oversight.

Expected output:

- a comment-triggered workflow run
- visible proof that normal automation and review controls remain in place

## Facilitator Actions

1. Name the human owner for the task.
2. State the output type out loud before using Copilot.
3. Confirm the work is inside approved AI-assistance scope.
4. Confirm the work is small enough to review in one sitting.
5. Choose the surface that will be used:

Surface options:

- local Copilot interaction for the PR review segment
- hosted or cloud-agent workflow for the issue-assignment segment
- repository workflow trigger for the final GitHub Actions segment

## Phase Gate Checkpoint

Implement Gate 1 here, before moving to any prompt or issue creation.

Gate 1 questions:

- Is there a named human owner?
- Is the output type explicit?
- Is the task inside approved usage scope?
- Can the work be reviewed as a small batch?
- Are legal, policy, and compliance questions already understood?
- Is the tool surface known?

If any answer is no, stop and narrow the task before continuing.



## Participant Prompts

Ask the group:

- Who is asking for the change, and who is accountable for the outcome?
- Which part of William's request should become the first small change?
- What should AI help produce in this phase, and what should a human still decide?
- What makes the endpoint request a better first slice than the full filtering feature?

## Key Points To Emphasize

- Intake happens before prompting.
- Small scope is a control, not a limitation.
- AI can help draft, summarize, and accelerate, but humans still own decisions, review, and release.
