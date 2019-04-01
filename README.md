# Cognisant Software Development Process

Cognisant develops software products for several companies. It uses the [Scrum](<https://en.wikipedia.org/wiki/Scrum_(software_development)>) framework, with development work arranged in two-week [sprints](<https://en.wikipedia.org/wiki/Scrum_(software_development)#Sprint>). Together, Cognisant and its customers define what development work goes into each sprint. This guide describes how that process works.

## Process

### Discovery

Users can add cards to the **Software Development** Trello board using a web form, hosted internally on the Intranet. This form asks users to provide:

- A title
- A description
- A proposed solution (optional)
- The impact on the business

When a user submits information using this form, a card is created in the **Inbox** list on the **Software Development** Trello board containing all the information they provided, along with their name and email address.

The team may also manually add cards to Trello at the request of management. When this happens, cards should follow the same format as above.

### Triage

From time to time, the team will go through all the cards in the **Inbox** list on the **Software Development** Trello board, and determine whether or not the idea adds value.

If it does, it gets moved to the **Idea Backlog** list. Otherwise, a comment is left on the card explaining the decision, and the card is archived.

The team may need to consult the user to determine whether the idea adds value. Any discussion or clarifications should added to the Trello card for future reference.

### Prioritisation

### Research

#### Writing Stories

#### UI Mockups

#### Business Review

#### Definition of Ready

### Estimating Effort

### Sprints

#### Sprint Kick-off

#### Selecting Stories

#### Generating Tasks

#### Daily Scrums

#### Definition of Done

It is important to have a well defined "definition of done", so that we know when we should call a story complete, and our customers know what to expect. This effectively forms an implicit set of acceptance criteria which is applied to every story. Our definition of done is expected to evolve over time, currently it includes the following criteria:

- Working code has been produced which satisfies all acceptance criteria listed on the Trello card.
- All code conforms to our chosen style for the relevant language. This rule will be relaxed for projects which have not yet been fully converted to conform with our style guide.
- Documentation has been produced. This should include a detailed description of any new functionality as well as a technical description of any configuration or infrastructure changes required to deploy it.
- Unit tests have been written where appropriate, and all existing tests are passing.
- Manual testing has been performed to ensure that the feature works as expected.
- The change has been demonstrated working to the rest of the team.
- The automated Teamcity build for the project is succeeding.
- A pull request has been submitted to the appropriate repository and reviewed by at least one other member of the team.
- Any required configuration or process changes have been made in Octopus Deploy, so that the change could be deployed with no additional work.

#### Demos

On the last day of a sprint, the team meets with relevant members of the business to present them the work the team completed during the sprint.

The demo is an opportunity for the business to provide feedback on the work. 
Often, any small problems the business points out can be corrected before the end of the day.

This meeting is also a chance for the team to explain how the completed work applies to the business' short term goals.

There is usually a discussion about when the work might be deployed to production and become accessible to users.

#### Retrospective

## Tools

### 1Password

### Planning Poker Cards

### Slack

### Sprint Board

### Trello

## Guidelines

### Design

### Development

- [Source Control](docs/source-control.md) (needs updating)
- Teamcity
- Octopus
- Code Style
  - [JavaScript](docs/code-style/javascript.md)
  - CSharp
