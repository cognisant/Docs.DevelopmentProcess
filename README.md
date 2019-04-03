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

Before a request can be worked on, it will be broken down into one or more story cards. Each story should be the smallest possible increment to the relevant system (or multiple systems) which delivers value to the business. It is possible that it will take many such increments to reach the final solution to the problem originally presented by the customer. This is fine provided that each individual story has value on its own.

The story card will be made up of three sections.

##### User Story
The user story is a concise description of the change, told from the perspective of the person who requested it. They usually take the following form:

As a `<type of user>`, I want `<their goal>` so that `<a reason>`.

##### Acceptance Criteria
The card will also define the minimum criteria which must be met for a solution to be accepted by the customer. These should be defined in conjunction with the customer stakeholders who will ultimately give the go-ahead for deployment of the solution (see also [Business Review](#business-review)).

##### Original Request
The original request will remain at the bottom of the Trello card in case we need to review it in future. This should not be modified.

##### Bug Cards
Some cards represent software defects rather than user stories. The description of these cards follows a slightly different format in order to describe the steps necessary to reproduce the bug. The sections are as follows:

- **How to Reproduce** - to describe any steps necessary to get the system into an appropriate state, followed by a description of the action which is not working as expected.
- **Expected Behaviour** - what the user expects to see when taking the action described above.
- **Actual Behaviour** - the actual (incorrect) behaviour exhibited by the system.
- **Impact** - a description of the business impact of the bug.

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
