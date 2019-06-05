# Trello - <https://trello.com>

## Software Development Boards

Each customer has a board on Trello to hold their backlog of change requests.

End users do not have access to modify cards on this board directly but can add comments and subscribe to the card to receive notifications on its progress.

### Lists

The software development board contains the following lists. Cards are moved by the team to reflect their development progress.

- **Current Epics** a set of cards representing all currently active epics.
- **Inbox** is a list of new requests fed by the feature request form.
- **Idea Backlog** for cards containing ideas worth exploring.
- **Researching Solution** for cards which are being actively researched and specified in the current sprint.
- **Product Backlog** for cards which have been fully specified and could potentially be worked on soon.
- **Current Sprint** for cards that are being worked on in the current sprint.
    - The title of this list includes the start and end dates of the sprint. These are updated at the start of every sprint to inform customers of when work in the current sprint might be completed.
- **Done** For completed work that has not yet begun UAT/Validation.
- **In Validation / UAT** for cards that are currently actively undergoing validation or user acceptance testing.
- **Ready To Deploy** for cards that have been validated and can be deployed.
- **Deployed** for completed work which has been deployed to production.

In general, the team tries to organise each list so that higher priority cards are nearer the top. This is meant as an indication of priorities rather than a strict contract for which cards will be worked on next.

### Trello Card Format

**Title**

They should contain a summary of the story; often this can be copied and pasted from the “I want...” portion of the story. Card titles may change as the problem and solutions are better understood.

**Estimates**

Effort estimates are stored in a custom field with the crystal ball symbol (🔮).

**Tags**

Trello cards get visibly tagged with one or more of the following:

- A blue tag indicating the epic to which they belong
- A red ‘Bug’ tag, indicating that this is a defect, rather than a new request.
- A green ‘Ready’ tag, indicating that the story is ready to be worked on.
- A pink ‘Regulatory Commitment’ tag, for stories that have been promised to regulators as corrective/preventative actions.
- One or more grey tags indicating the system(s) that are impacted by the change. These are not visible on the face of the card, but allow easy filtering by a system.

**Descriptions**

Card descriptions are added to by the development team. To begin with, they include the description provided by the original author. Once agreed, the development team writes a specification that explains the scope of the work and the steps necessary to complete it. The format of a description is described in the [Writing Stories](#writing-stories) section.

## Retrospective Board

The team uses a board on Trello to track both potential retrospective discussion points, and actionable tasks that have been identified as potential future process improvements.