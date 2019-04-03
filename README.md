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

Before a story can be worked on, the business member who submitted the original Trello card, or another relevant member of the business, must approve the story.  
This ensures that the story accurately describes the original problem, and includes acceptance criteria for an appropriate solution.  
Simplisitc stories, such as bug descriptions, do not require a business review.

Sometimes the team will have envisaged a solution to the problem, which is significantly different from the solution originally suggested by the member of the business.  
In these instances, a more in-depth discussion may be necessary to explain the story to the member of the business.

If the business member is not happy with the story, the team will rewrite the story to address their concerns.

#### Definition of Ready

### Estimating Effort

### Sprints

#### Sprint Kick-off

#### Selecting Stories

#### Generating Tasks

#### Daily Scrums

 On each day of a sprint at 1:30pm the team gathers around the sprint board for a meeting called the “daily scrum”. Every team member who is able to stand should do so; this helps to encourage brevity. During the daily scrum each team member answers the following three questions:

- What did you do since the last meeting to help the team finish the Sprint?
- What do you plan to do before the next meeting to help the team finish the Sprint?
- What obstacles are getting in the team's way?

 The daily scrum meeting is not used as a problem-solving or issue resolution meeting. Issues that are raised are usually dealt with immediately after the meeting.

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

On the last day of a sprint, after the demo, the team has a retrospective meeting.

Members of the team take it in turns to bring snacks for the whole team to this meeting.

During the retrospective, the team discusses how the sprint went, reflecting on what went well during the sprint, any issues that came up, and how productive the sprint was.

The main objective of these meetings is to identify improvements that could be made to the development process.

During the sprint, the team uses the Retrospective Trello board to record any points they think should be discussed at the retrospective.  
At the meeting, the team will review all of the discussion points added to the board.  
If necessary, the team will attempt to think of a systematic method of addressing a point raised.  
Often discussion points are simply something to keep in mind during future sprints, or a small problem that can be immediately addressed with a simple action.

Any possible process improvements agreed upon by the team will be trialled in a future sprint, then discussed and refined during that sprint's retrospective.

An example of a process improvement derived from a retrospective meeting is [the work in progress limit](https://github.com/cognisant/Docs.DevelopmentProcess/blob/dev-with-retrospective/docs/work-in-progress-limit.md).

#### Learning

Each sprint, two team members are selected to spend a portion of their time learning. This training should be focused on technologies/tools/techniques which could be of benefit to the team in future. Team members have access to the company Pluralsight subscription which provides an array of video training courses, but are also free to use other resources.

#### Tech Debt

Each sprint, two team members are selected to spend a portion of their time working on tech debt. This allows us time to make technical improvements to our projects which have not been directly requested by the business, but are nonetheless valuable. Examples of this type of work might include making improvements to our build/deployment infrastructure or upating dependencies to ensure we have the latest security patches.

## Tools

### 1Password

1Password is the password manager the team uses to securely store and share work-related passwords.

Team members use private vaults to manage passwords for their own work-related accounts.

There is also customer-specific vaults. These are used for managing shared credentials associated with a specific customer, or a software system used by that customer.

If a team member needs to use the credentials of a shared account, they can find them in the relevant vault.

### Planning Poker Cards

### Slack

[Slack](https://slack.com) is used by the development team as a communication tool. This allows direct person to person communication, as well as channels dedicated to a particular topic which can be joined by many team members.

The `#general` channel exists by default, and can be used for general team discussion and announcements.
Channels regarding a particular project should be prefixed with `proj`, for example `#proj-order-manager`.
Temporary channels for ad-hoc discussions should be prefixed with `temp`, for example `#temp-balances`.
Some channels are used with third party integrations to provide notifications. These should be prefixed with `bot`, for example `#bot-monitoring`.


### Sprint Board

The development team has a large, physical whiteboard in their workspace called the _sprint board_. The sprint board has three main sections, each used to track a different aspect of the sprint.

#### Sprint Progress Columns

Kanban columns occupy most of the sprint board. The team uses these to track the progress of work during a sprint. See [Tracking Progress](#Tracking-Progress) for more details.

Each task is represented by a Post-it on the board. These Post-its move through the columns on the board throughout the sprint. At the end of a sprint, most (if not all) of the task Post-its will have migrated from the “To do” column through the “Doing” and “Verify” columns to the “Done” column.

#### Distractions

There is a reserved area on the sprint board for distractions. Development team members add a Post-it to this area whenever they deviate from sprint-related work. Team members add the duration of the distraction and their initials to the Post-it. The development team reviews distractions during the [retrospective](#Retrospective).

#### Retrospective Goals

There is an area on the sprint board for highlighting the current retrospective goals. These act as constant reminders to the team about what the agreed goals are for improving the process.

### Trello

## Guidelines

### Design

### Development

- [Source Control](docs/source-control.md) (needs updating)
- Teamcity
- Octopus
- Code Style
  - [JavaScript](docs/code-style/javascript.md)
  - [C#](docs/code-style/csharp.md)
