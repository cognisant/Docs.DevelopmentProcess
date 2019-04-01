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

#### Tracking Progress

During the sprint, the teams progress on the tasks generated during the sprint kick-off are tracked using Post-it notes on a [large physical whiteboard](#sprint-board). 

![The Cognisant development team sprint board (captured mid-sprint)](/images/sprint-board.jpeg "The sprint board (captured mid-sprint)")

The board is arranged into columns named 'to do', 'doing', 'verify', and 'done'. Usually the tasks for each story which has been included in the sprint are grouped into horizontal lanes. Extra-large Post-it notes are placed on the far left of the board to indicate the lanes. Occasionally, stories may be deemed too small to be broken down into fine-grained tasks. These will instead be grouped into a 'Single Card Stories' lane at the top of the board.

When starting work a team member will take a single task Post-it, add their initials, and place it in the 'doing' column. When the work is complete, the task will be moved to the 'verify' column, and begin the next task. 

Tasks remain in the verify column until the code has been reviewed by another team member. Once tasks have been reviewed, they can be moved to the 'done' column. Sometimes it is possible to review a single task, but in practice an entire story will often be reviewed as a whole. If changes are requested as part of the review, these should be recorded onto additional Post-its and placed in the 'to do' column.

In order to minimise the quantity of partially complete stories at the end of a sprint, a limit is imposed on the number of work in progress stories. Currently, this limit is set at 3 stories.

The sprint board is also used to track distractions which occur during a sprint. These are recorded on post-it notes with a description and a rough estimate of time spent. A distraction is anything that prevented a team member from spending time on planned sprint tasks e.g time spent in meetings, or responding to support tickets. These can be used to identify trends in impediments, and account for lower than expected achievement during a sprint.

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
