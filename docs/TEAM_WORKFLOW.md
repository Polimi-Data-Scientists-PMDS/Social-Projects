# Team workflow

This document describes how we intend to collaborate. Repository permissions and branch protection still need to be configured.

## Branches

All team members, including the project lead, normally work on branches and propose changes to `main` through pull requests (PRs). Start new work from an up-to-date base and coordinate the work with the team. Specific development branches and their names will be decided as the project takes shape.

We use two kinds of branches:

- **Ongoing development branches** support substantial features or subsystems. They remain available while that work continues, potentially across several PRs, and are removed when the work is complete and the branch is no longer needed.
- **Short-lived branches** address a specific issue, fix, refactor or similar task. Once the work is ready, open a PR. Remove the branch when its work and PR are finished and it is no longer needed.

We will investigate whether short-lived branch deletion can be automated without removing ongoing development branches. Until then, check and clean up branches manually when appropriate.

## Pull requests

For a short-lived task, open a PR when the change is ready for review. For ongoing development, open PRs periodically or at meaningful milestones rather than waiting for the entire subsystem to be finished. Early work may lend itself more to milestone-based PRs; later, a regular cadence may be more useful. Agree on the timing according to the work.

Each PR should represent a coherent, working state: the intended change works and the relevant tests pass. Explain what changed, how it was checked, and any limitations or open questions. If a check cannot be run, say so. Draft PRs can be used for feedback before the work is ready for approval.

Ongoing work can continue after a milestone, but later commits pushed to a PR's source branch are automatically included in that open PR. If development needs to continue independently while a stable milestone is reviewed, coordinate a separate branch for the PR or otherwise ensure that the submitted state remains clear. After merging, keep the ongoing development branch and bring it up to date with `main` as needed before the next milestone.

## Review and merging

Anyone on the team may review a PR, ask questions, suggest changes and approve it; reviews do not have to be performed by the project lead. The author responds and updates the PR as needed. For now, the project lead gives the final approval after any other reviews and is the only person who merges PRs into `main`. Another person's approval does not replace the lead's final approval. Reviewing, approving and merging are separate actions.

The lead may later designate additional required approvers or people allowed to merge. Update this agreement and the repository settings when that decision is made.

## Repository settings to arrange later

The lead will arrange branch protection and permissions separately, with help from other coding agents if desired. The intended setup requires PRs for normal work and restricts merging to the lead for now. The preferred setup also allows the lead to push directly to `main` when needed; the team should verify whether the available GitHub settings can enforce these distinctions and document any bypasses or limitations. No settings have been configured by this document.

## Working together

- Agree on a task or milestone and its expected outcome; record open questions in the task or PR.
- Share work early, especially when a decision affects another person's work.
- Do not commit API keys, tokens, credentials or private content. Agree on a safe way to share access when integrations are needed.
- Keep project decisions and setup instructions current as the team learns.
