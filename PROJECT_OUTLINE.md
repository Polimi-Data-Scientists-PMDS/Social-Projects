# PMDS social media agent — project outline

**Status:** Early draft for team discussion. The detailed scope and implementation plan are still to be defined.

## Goals

- Build an assistant that helps PMDS create social media posts and reduces repetitive work for the team.
- Give the project team practical experience with agent development, external integrations and deployment technologies used in industry.

## Intended workflow

A team member sends a request through Telegram, together with relevant links and images. The agent asks for essential missing information and prepares an editable post in Figma using the existing PMDS template, plus a separate caption. The member can request changes, and a person reviews the result before publication. This is the intended workflow, not a tested implementation.

## Technical direction

- Implement the agent in **Python**, starting with **LangChain**. Consider LangGraph later only if needed.
- Provide access through **Telegram** and investigate using **OpenCode with Figma's MCP connector** for the Figma work. The required editing, image handling and remote operation still need to be validated.
- Develop locally first. To make the agent available to the wider team, aim to run it on a **virtual machine**, potentially using **Google Cloud or AWS**. The provider, costs and deployment details remain open.

## Next steps: define the project in detail

The immediate next step is to agree with the team on what to build before choosing an implementation plan:

1. **Define the first useful version:** choose the post types and template variants to support, the essential features, and what can wait.
2. **Specify the workflow:** decide what information, links and images a request needs; which follow-up questions to ask; and how drafts, captions, reviews and revisions should work.
3. **Agree on success criteria:** use realistic PMDS requests to define acceptable drafts and captions, how the team will evaluate them, and how much manual correction is acceptable.
4. **Test the Figma approach:** investigate whether OpenCode and Figma's MCP connector can edit the existing template, insert supplied images and support revisions, authentication and eventual remote operation.
5. **Plan operation and access:** decide who can use the bot, how requests and failures are handled, and what cloud resources, budget and credentials are available.
6. **Turn the decisions into a plan:** document the agreed scope, unresolved questions and milestones, then select the first prototype to build.

