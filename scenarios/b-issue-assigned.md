# Scenario B: Issue Instructions For GitHub Copilot

This file contains an issue-ready set of instructions that can be assigned to GitHub Copilot to implement a new feature in the project.

## Suggested Issue Title

Add breed and availability filters to the dog list page

## Suggested Issue Body

### Background

The website currently lists all dogs in the database. This worked when the shelter only had a few dogs, but the list has grown and it is now harder for adopters to find the dogs they are interested in.

We want to improve the browsing experience by adding filters so a user can:

- select a breed of dog
- choose to only show dogs that are available for adoption

### Goal

Update the project so the dog list page supports filtering by breed and availability.

### Project Context

- The backend is a Flask application.
- The frontend is an Astro application.
- This change will likely require updates to both the backend and frontend.

Relevant files to inspect first:

- `app/server/app.py`
- `app/client/src/components/DogList.astro`

### Requirements

Implement the feature with the following behavior:

1. Add a breed filter to the dog list page.
2. Add an availability filter so users can show only dogs available for adoption.
3. Provide the breed filter as a dropdown containing all available breeds.
4. Provide the availability filter as a checkbox.
5. Automatically refresh the displayed dog list whenever either filter changes.

### Backend Expectations

1. Update the existing dog-listing behavior so it can filter results by breed.
2. Update the existing dog-listing behavior so it can filter results by adoption availability.
3. Keep the implementation consistent with the current Flask and SQLAlchemy patterns already used in the project.

### Frontend Expectations

1. Update the dog list page UI to render the dropdown and checkbox.
2. Ensure the page requests and displays filtered results when the user changes a filter.
3. Keep the UI changes minimal and consistent with the existing page structure.

### Constraints

1. Keep the change focused on this feature.
2. Do not refactor unrelated areas of the application.
3. Reuse existing project patterns and styles where possible.
4. If you need to make assumptions, keep them minimal and align them to the current codebase.

### Validation

Before considering the work complete:

1. Confirm the page loads and the filters are visible.
2. Confirm the dog list updates when the breed dropdown changes.
3. Confirm the dog list updates when the availability checkbox changes.
4. Run the backend tests from `app/server` using `python -m unittest`.

### Expected Output

Please create a pull request that:

1. implements the feature
2. keeps the scope limited to breed and availability filtering
3. includes a clear summary of what changed in the backend and frontend

## Notes For The Facilitator

If you want to assign this issue to GitHub Copilot during the demo, use the issue body above as-is or trim it slightly for time. It is written to be explicit enough for Copilot to act on while still leaving the audience room to review scope, assumptions, and quality.
