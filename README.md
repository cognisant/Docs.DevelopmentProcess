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

The team uses numeric 'effort' points to represent the magnitude/difficulty of stories.  
These points do not equate to a duration of time it would take the team to complete the story. They are more abstract.

After a story has been specified, the team estimates how many points the story is, this is done as a group using **planning poker cards**.  
The team estimates a points value of a story using their knowledge of the points values of previously completed stories and their magnitude/difficulty.

The smallest of tasks are assigned 1 effort point. A 1 point story could be typo correction or an extremely simple bug fix.  
The greatest effort value a story can be assigned is 21. 

The number of points the team completes per sprint is used to track productivity. 

How many points the team typically completes in a sprint is considered when planning which 'ready' stories should be included in a sprint.

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
