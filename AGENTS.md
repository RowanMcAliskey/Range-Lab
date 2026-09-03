# Range Lab Repository Guidelines

## Core Project Rule

Range Lab is an existing, working mobile-first golf practice application. It is not a blank-slate project.

Preserve existing behavior unless a requested change specifically requires modifying it. Prefer incremental, targeted changes over rewrites or broad refactors.

Do not make unrelated improvements while completing a specific task.

## Project Structure

Range Lab is currently a dependency-free static web application.

`index.html` contains the complete product:

- HTML markup
- CSS
- browser-side JavaScript

JavaScript is organized conceptually into:

- `StorageService`
- `Data`
- `Analytics`
- `Generator`
- `UI`
- `App`

`README.md` documents the product and basic usage.

Do not introduce frameworks, build systems, package managers, major dependencies, databases, or a new architecture without first explaining why they are necessary and receiving explicit approval.

Simple architecture is preferred.

## Product & UX Requirements

Preserve the existing clean, restrained, Apple-style visual language.

Range Lab is mobile-first.

Important UX principles:

- One-handed use matters.
- Buttons should remain large and easy to tap.
- Important actions should not require unnecessary scrolling.
- Typography should remain clear and high contrast.
- Preserve accessibility attributes and focus behavior.
- Preserve reduced-motion support.
- Do not redesign screens unless specifically requested.

## Data Safety

Existing user data and session history are important.

Range Lab currently stores data using IndexedDB with a localStorage fallback.

Do not:

- change storage schemas casually
- delete or reset user data
- remove migration logic
- introduce remote synchronization
- add tracking
- add external data calls

unless the task explicitly requires it and the impact has been explained first.

Never commit API keys, passwords, tokens, or other secrets.

## Development Behavior

Before making a non-trivial change:

1. Inspect the relevant existing code.
2. Explain the proposed approach briefly.
3. Make the smallest reasonable change.
4. Avoid touching unrelated code.
5. Test the affected behavior.
6. Report exactly what changed and what was tested.

For significant architectural changes, explain the tradeoffs in plain English before implementing them.

Do not rewrite working sections merely to make them more elegant.

The application should remain usable after every approved change.

## Testing

There is currently no automated test suite.

For relevant changes, manually test the affected workflow and check for browser console errors.

When appropriate, also verify:

- onboarding
- bag editing and saved distances
- Random Practice
- Play the Course
- feedback entry
- reset flow
- session pause/resume
- interrupted-session recovery
- session completion
- history
- analytics
- CSV export
- mobile viewport behavior
- persistence after reload

Do not claim a feature is tested if it was not actually tested.

## Local Development

No install or build step is currently required.

To serve the project locally:

```sh
python3 -m http.server 8000
```
