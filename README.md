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

The business intermittently advises the team on their current short-term and long-term goals.

At the start of a sprint, the team tries to pick stories relating to the business' current priorities to include in the sprint.

Priorities are also important to keep in mind during **backlog refinement** meetings.  
It is more important for the team to specify and estimate stories relating to the business' urgent priorities, instead of reviewing more general feature requests.

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

#### Bug Cards
Some cards represent software defects rather than user stories. The description of these cards follows a slightly different format in order to describe the steps necessary to reproduce the bug. The sections are as follows:

- **How to Reproduce** - to describe any steps necessary to get the system into an appropriate state, followed by a description of the action which is not working as expected.
- **Expected Behaviour** - what the user expects to see when taking the action described above.
- **Actual Behaviour** - the actual (incorrect) behaviour exhibited by the system.
- **Impact** - a description of the business impact of the bug.

#### Epics

Several separate stories may relate to a single business objective.

Relatively large business goals which include the completion of several stories, are referred to as 'epics'.

All of the stories which belong to an epic will be labelled (on their Trello card) with the name of the relevant epic.

On the **Software Development** Trello board, there is a 'Current Epics' column containing cards describing the epics which some of the stories on the board currently belong to.

#### UI Mockups

For stories whose implementation will require substantial user interface changes, UI mockups of one or more potential solutions will be added to the card. This helps team members estimate more accurately, and customers more easily imagine how the feature might eventually work. These mockups are be treated as a guide, not necessarily a contract for exactly how the final UI will work.

#### Business Review

Before a story can be worked on, the business member who submitted the original Trello card, or another relevant member of the business, must approve the story.  
This ensures that the story accurately describes the original problem, and includes acceptance criteria for an appropriate solution.  
Simplisitc stories, such as bug descriptions, do not require a business review.

Sometimes the team will have envisaged a solution to the problem, which is significantly different from the solution originally suggested by the member of the business.  
In these instances, a more in-depth discussion may be necessary to explain the story to the member of the business.

If the business member is not happy with the story, the team will rewrite the story to address their concerns.

#### Definition of Ready

A Trello card can be considered ready to be worked on if it meets the criteria defined by the INVEST acronym:

- *I*ndependent. The story must be actionable and "completable" on its own. It shouldn't be inherently dependent on another story.
- *N*egotiable. Until it's actually being done, it needs to be able to be rewritten. Allowance for change is built in.
- *V*aluable. It actually delivers value to a customer or stakeholder.
- *E*stimable. You need to be able to size it. (Using the process defined in the [Estimating Effort](#estimating-effort) section)
- *S*mall. The story needs to be small enough to be able to estimate and plan for easily. If it is too big, rewrite it or break it down into smaller stories.
- *T*estable. The story must have a test it is supposed to pass in order to be considered complete. (These are defined in our Trello cards under the heading "Acceptance criteria")

Once the card is ready it will be tagged using the green 'Ready' tag on Trello. It is then eligible for selection during the next [Sprint Kick-off](#sprint-kick-off).

### Estimating Effort

The team uses numeric 'effort' points to represent the magnitude/difficulty of stories.  
These points do not equate to a duration of time it would take the team to complete the story. They are more abstract.

After a story has been specified, the team estimates how much effort they believe it will take to develop a solution to meet the acceptance criteria. Each member of the team has a deck of [planning poker cards](planning-poker-cards) which are made up of the fibonacci numbers from 1-21.

The process for estimating a story is as follows.

1. One of the members of the team presents the card to the team, describing the problem and going over the acceptance criteria.
2. A discussions takes place over changes required to systems, and the extent of testing required.
3. Each member of the team votes on the amount of effort required by selecting a card from their deck of [planning poker cards](planning-poker-cards), with 1 being the lowest and 21 being the largest.
4. The cards are revealed
   1. If everyone is within 1 card (e.g. 3 and 5 or 8 and 13) then the effort for the story is the average of the cards .
   2. If there is a wider spread (e.g. 3, 5 and 8), then the high and low cards task about why they voted as they did, and then another vote takes place.

### Sprints

A sprint is a time-box during which a ["Done"](#definition-of-done), useable, and potentially releasable product increment is created. At Cognisant we work in two week sprints starting on a Monday and ending on a Friday. A new Sprint starts immediately after the conclusion of the previous Sprint. 

#### Sprint Kick-off

On the first Monday of a sprint, at 10am, the sprint begins with a kick-off meeting.
During this meeting the team engages in the following activities to prepare for the sprint:

- For any stories partially complete at the end of the previous sprint, the remaining work should be discussed and [estimated](#estimating-effort).
- A number of additional stories should be selected, which the team will aim to complete during the new sprint.
  - The number of story points chosen is slightly higher (+3) than the number achieved in the previous sprint. If necessary this number can be scaled to account for planned absences or special business circumstances.
- Each new story is discussed and broken down into a set of fine-grained technical tasks. These tasks are transcribed onto Post-it notes and attached to the sprint board to allow us to track work during the sprint. 
  - Occasionally during this breakdown, we will discover some complexity in implementing the feature which had not previously been considered. If this happens, we may choose to re-estimate the story and, if necessary, change the set of stories selected for the sprint.

#### Tracking Progress

During the sprint, the teams progress on the tasks generated during the sprint kick-off are tracked using Post-it notes on a [large physical whiteboard](#sprint-board). This gives the entire team visibility of sprint progress at all times.

![The Cognisant development team sprint board (captured mid-sprint)](/images/sprint-board.jpeg "The sprint board (captured mid-sprint)")

The board is arranged into columns named 'to do', 'doing', 'verify', and 'done'. Tasks belonging to each story in the sprint are grouped into horizontal lanes signified by a title card on the far left.
Occasionally, stories may be deemed too small to be broken down into fine-grained tasks. These will instead be grouped into a 'Single Card Stories' lane at the top of the board.

When starting work a team member will take a single task Post-it, add their initials, and place it in the 'doing' column. When the work is complete, the task will be moved to the 'verify' column, and begin the next task. 

Tasks remain in the verify column until the code has been reviewed by another team member. Once tasks have been reviewed they can be moved to the 'done' column. Sometimes it is possible to review a single task, but in practice an entire story will often be reviewed as a whole. If changes are requested as part of the review, these should be recorded onto additional Post-its and placed in the 'to do' column.

In order to minimise the quantity of partially complete stories at the end of a sprint, a limit is imposed on the number of work in progress stories. Currently, this limit is set at 3 stories.

The sprint board is also used to track distractions which occur during a sprint. These are recorded on post-it notes with a description and a rough estimate of time spent. A distraction is anything that prevented a team member from spending time on planned sprint tasks e.g time spent in meetings, or responding to support tickets. These can be used to identify trends in impediments, and account for lower than expected achievement during a sprint.

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

During [estimation](#estimating-effort) sessions, planning poker cards containing Fibonacci numbers 1-21 are used to allow team members to choose then simultaneously reveal their estimate. 6 player decks can be purchased from [https://agilestationery.co.uk/products/estimation-poker-cards](https://agilestationery.co.uk/products/estimation-poker-cards) with the discount code `THANKYOU` to receive 20% off.

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

Each customer will have their own board on [Trello](https://trello.com) to hold their backlog of change requests.

End users do not have access to modify cards on this board directly but can add comments and subscribe to the card to receive notifications on its progress.

#### Trello Card Format

**Title**

They should contain a brief summary of the story; often this can be copied and pasted from the "I want..." portion of the story. Card titles may change as the problem and solutions are better understood.

**Estimates**

Effort estimates are stored in a custom field with the crystal ball symbol (🔮).

**Tags**

Trello cards will be visibly tagged with one or more of the following:

- A blue tag indicating the epic to which they belong
- A red "Bug" tag, indicating that this is a defect, rather than a new request.
- A green "Ready" tag, indicating that the story is ready to be worked on.
- A pink "Regulatory Commitment" tag, for stories that have been promised to regulators as corrective/preventative actions.
- One or more grey tags indicating the system(s) which will be impacted by the change. These are not visible on the face of the card, but allow easy filtering by system.

**Descriptions**

Card descriptions will be added to by the development team. To begin with, they will include the description provided by the original author. Once agreed, the development team will write a specification that explains the scope of the work and the steps necessary to complete it. The format of a description is described in the [Writing Stories](#writing-stories) section.

### Lists

The software development board will contain the following lists. Cards will be moved by the team to reflect their development progress.

- **Current Epics** a set of cards representing all currently active epics.
- **Inbox** is a list of new requests fed by the feature request form.
- **Idea Backlog** once a card from the inbox has been reviewed by the team, it will be moved here.
- **Researching Solution** for cards which are being actively researched and specified in the current sprint.
- **Product Backlog** for cards which have been fully specified and could potentially be worked on soon.
- **Current Sprint** for cards that are being worked on in the current sprint.
- **Done** For completed work that has not yet begun UAT/Validation.
- **In Validation / UAT** for cards that are currently actively undergoing validation or user acceptance testing.
- **Ready To Deploy** for cards that have been validated and will be deployed soon.
- **Deployed** for completed work which has been deployed to production.

In general, the team tries to organize each list so that higher priority cards are nearer the top. This is meant as an indication of priorities rather than a strict contract for which cards will be worked on next.

## Guidelines

### Design

### Development

- [Source Control](docs/source-control.md) (needs updating)

#### Teamcity
[TeamCity](https://www.jetbrains.com/teamcity/) is a Java-based build management and continuous integration server from JetBrains.

Each Cognisant project will have a corresponding configuration in Teamcity created at the outset. When code is committed to the Git repository, it will be automatically built and tested by the Teamcity server. The resulting packages are published to a nuget feed, to be consumed by [Octopus Deploy](#octopus-deploy). 

The build status is automatically pushed back as a status check on the Github pull request. This prevents any change from being merged if it does not build and pass all automated tests.

#### Octopus Deploy

[Octopus deploy](https://octopus.com) is a deployment automation server designed to make it easy to orchestrate releases and deploy applications, whether on-premises or in the cloud.

Each Cognisant project will have a corresponding project in octopus deploy. The project will contain a definition of the deployment workflow, usually deploying one or more packages from the Teamcity nuget feed.

Each project may also have a number of variables defined. Upon deployment, Octopus is capable of replacing placeholder values in config files with the appropriate value for the environment into which the software is being deployed (Test, Production, etc).

For software which is deployed to multiple customers, Octopus supports the concept of "Tenants". This allows for example Bath ASU and Pharmaxo to receive the same system, deployed to separate servers and with bespoke configuration variables.

#### Code Style
  - [JavaScript](docs/code-style/javascript.md)
  - [C#](docs/code-style/csharp.md)
