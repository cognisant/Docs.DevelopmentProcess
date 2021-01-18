# Corsham Science Software Development Process

The development team within Corsham Science develops bespoke software products for use within the QPHL group. This document describes the processes followed to produce that software.

## Contents

1. [Process](#Process)
   1. [Discovery](#Discovery)
   1. [Triage](#Triage)
   1. [Research](#Research)
      1. [User Stories](#User-Stories)
      1. [Bugs](#Bug-Cards)
      1. [Technical Improvements](#Technical-Improvements)
      1. [Epics](#Epics)
      1. [UI Mockups](#UI-Mockups)
      1. [Definition of Ready](#Definition-of-Ready)
   1. [Estimating Effort](#Estimating-Effort)
   1. [Sprints](#Sprints)
      1. [Sprint Kick-off](#Sprint-Kick-off)
      1. [During the Sprint](#During-the-Sprint)
      1. [End of Sprint](#End-of-Sprint)
1. [Tools](#Tools)
   1. [Planning Poker Cards](#Planning-Poker-Cards)
   1. [Sprint Board](#Sprint-Board)
   1. [Post-Its](#Post-Its)
   1. [Trello](#Trello)
   1. [Slack](#Slack)
   1. [TeamCity](#TeamCity)
   1. [Octopus Deploy](#Octopus-Deploy)
   1. [1Password](#1Password)
1. [Ceremony Agenda](#Ceremony-Agenda)
1. [Guidelines](#Guidelines)
   1. [Design](#Design)
   1. [Development](#Development)

## Process

The development team uses the [Scrum](<https://en.wikipedia.org/wiki/Scrum_(software_development)>) framework, with development work arranged in two-week [sprints](<https://en.wikipedia.org/wiki/Scrum_(software_development)#Sprint>). Together, Corsham Science and stakeholders from throughout the QPHL group define what development work goes into each sprint.

### Discovery

To request new software functionality or report a problem with a software system, users can add cards to the [Software Development](docs/trello.md#software-development-boards) Trello board using a web form, hosted internally on the Intranet. This form asks users to provide:

- A title
- A description
- A proposed solution (optional)
- The impact on the business

When a user submits information using this form, a card is created in the **Inbox** list on the [Software Development](docs/trello.md#software-development-boards) Trello board containing all the information they provided, along with their name and email address.

The team may also manually add cards to Trello at the request of management. When this happens, cards should follow the same format as above.

### Triage

From time to time, the team goes through all the cards in the **Inbox** list on the [Software Development](docs/trello.md#software-development-boards) Trello board, to determine whether or not each idea adds value.

If an idea is valuable, it gets moved to the **Idea Backlog** list. Otherwise, a comment is left on the card explaining the decision, and the card is archived.

The team may need to consult the user to determine whether the idea adds value. Any discussion or clarifications should be added to the Trello card for future reference.

### Research

#### User Stories

Before a request can be worked on, it gets broken down into one or more story cards. Each story should be the smallest possible increment to the relevant system (or multiple systems) which delivers value to the business. It is possible that it takes many such increments to reach the final solution to the problem initially presented by the customer. This is fine provided that each story has value on its own.

The story card is made up of three sections.

##### Story

The story is a concise description of the user’s problem, told from the perspective of the person who requested it. They usually take the following form:

As a `<type of user>`, I want `<their goal>` so that `<a reason>`.

Good stories are solution-agnostic.

##### Acceptance Criteria

The card also defines the minimum criteria which must be met for a solution to be accepted by the customer. These should be defined in conjunction with the customer stakeholders who ultimately give the go-ahead for deployment of the solution (see also: [Business Review](#business-review)).

##### Original Request

The original request remains at the bottom of the Trello card in case we need to review it in future. This should not be modified.

#### Bugs

Some cards represent software defects rather than user stories. Descriptions of these cards follow a slightly different format to describe the steps necessary to reproduce the bug. The sections are as follows:

- **How to Reproduce** - any steps necessary to get the system into an appropriate state, followed by a description of the action which is not working as expected.
- **Expected Behaviour** - what the user should see when taking the action described above.
- **Actual Behaviour** - the actual (incorrect) behaviour exhibited by the system.
- **Impact** - the business impact of the bug.

#### Technical Improvements

Some cards represent [technical improvements](https://en.wikipedia.org/wiki/Technical_Improvements) that has accumulated over time for various reasons, these are not directly requested by the business, but should still be valuable. Examples of this type of work might include updating dependencies, improving the quality or quantity of automated testing or improving the build/deployment infrastructure.

Technical improvements cards are managed on a separate [tech improvements](docs/trello.md#Tech-Improvements-Board) Trello board until they are deemed ready to be worked on, at which point they are added to the product backlog of the relevant [Software Development](docs/trello.md#software-development-boards) Trello board and will be available for [estimation](#Estimating-Effort).

The format of a technical improvements card is not fixed due to the wide ranging nature of these tasks, however in all cases there should be a definition of what ‘done’ looks like for that specific card. For software changes this will usually be writing some acceptance criteria, that can be used with the [definition of done](docs/definition-of-done.md).

#### Epics

Relatively large business goals which include the completion of several stories are referred to as ‘epics’. All of the stories which belong to an epic are labelled (on their Trello card) with the name of the relevant epic.

The **Current Epics** column (of the [Software Development](docs/trello.md#software-development-boards) Trello board) contains cards describing epics to which some of the stories on the board currently belong.

#### UI Mockups

For stories whose implementation require substantial user interface changes, UI mockups of one or more potential solutions are added to the card. This helps team members estimate more accurately, and customers more easily imagine how the feature might eventually work. These mockups should be treated as a guide, not necessarily a contract, for exactly how the final UI works.

#### Definition of Ready

A Trello card can be considered ready to be [estimated](#estimating-effort) if it meets the criteria defined by the **INVEST** mnemonic, and has been business reviewed.

##### INVEST

- **I**ndependent. The story must be actionable and completable on its own. It shouldn’t be inherently dependent on another story.
- **N**egotiable. Until it’s being done, it needs to be able to be rewritten. Allowance for change is built in.
- **V**aluable. It delivers value to a customer or stakeholder.
- **E**stimable. You need to be able to estimate the size of it.
- **S**mall. The story needs to be small enough to be able to estimate and plan for easily. If it is too big, rewrite it or break it down into smaller stories.
- **T**estable. The story must have a test it is supposed to pass to be considered complete (these are defined in our Trello cards under the heading ‘Acceptance criteria’).

##### Business Review

Once the team believes a card is ready to be worked on, the business member who submitted the original Trello card, or another relevant member of the business, must approve the story. This ensures that the story accurately describes the original problem, and includes acceptance criteria for an appropriate solution.

If the business member is not happy with the story or there are points that need clarification, the team will rewrite the story to address their concerns.

Simplistic stories, such as bug descriptions, do not require a business review.

### Estimating Effort

The team uses numeric ‘effort’ points to represent the magnitude/difficulty of stories.

These points do not equate to a duration of time it would take the team to complete the story. They are more abstract.

After a story has been specified, the team estimates how much effort they believe it will take to develop a solution that meets the acceptance criteria, and make the story meet the [definition of done](docs/definition-of-done.md). Each member of the team has a deck of [planning poker cards](#planning-poker-cards) which are made up of the Fibonacci numbers from 1–21.

The process for estimating a story is as follows.

1. One of the members of the team presents the card to the team, describing the problem and going over the acceptance criteria.
2. Each member of the team votes on the amount of effort required by selecting a card from their deck of [planning poker cards](#planning-poker-cards), with 1 being the lowest and 21 being the largest.
3. The cards are revealed
   1. If everyone is within 1 card (e.g. 3 and 5 or 8 and 13), then the effort for the story is the average of the cards.
   2. If there is a wider spread (e.g. 3, 5 and 8), the team members who voted the highest and lowest explain why they voted as they did. For example, they might discuss the extent of required changes to systems, or the magnitude of testing required. The team then votes again.

If, during estimation, a member of the team votes that a story's effort value is 21, this is likely a sign that the story is not actually **S**mall (see [INVEST](#Invest)) and the team will discuss how it can be split into smaller stories to work on.

### Sprints

A sprint is a time-box during which a ‘[Done](docs/definition-of-done.md)’, usable, and potentially releasable product increment is created. At Corsham Science we work in two-week sprints starting on a Monday and ending on a Friday. A new Sprint starts immediately after the conclusion of the previous Sprint.

#### Sprint Kick-off

On the first Monday of a sprint, at 10 am, the sprint begins with a kick-off meeting.

During the sprint kick-off meeting the team decides what will be worked on during the sprint.

##### Stories

During this meeting the team engages in the following activities to prepare which user stories, bug cards and technical improvements will be worked on during the sprint:

- For any stories partially complete at the end of the previous sprint, the remaining work should be discussed and [estimated](#estimating-effort).
  - Partially complete stories are not guaranteed to be included in the next sprint, a change in business priority may require a different set of stories to be worked on.
- A set of stories should be selected, which the team aims to complete during the new sprint.
  - The stories picked should primarily consist of those relating to the business’ current priorities.
  - The number of story points chosen is slightly higher (+3) than the number achieved in the previous sprint. If necessary, this number can be scaled to account for planned absences or special business circumstances.
- Each new story is discussed and broken down into a set of fine-grained technical tasks. These tasks are transcribed onto Post-it notes and attached to the [sprint board](#the-sprint-board) to allow us to track work during the sprint.
  - If a story is deemed small enough it is left as a single large story Post-it.
  - A story may need to be branched from one different than master, in cases like this the branch name should be written on the story's Post-it.
  - A story may be considered a high-priority story, this could be for many reasons including an immediate business need, or a story blocking other work either inside the team, or the business. In this case the story will be marked with an asterisk (\*) on the sprint board.
  - Occasionally during this breakdown, the team discovers some complexity in implementing the feature which had not previously been considered. If this happens, the team may choose to re-estimate the story and, if necessary, change the set of stories selected for the sprint.

##### Retrospective Goals

The team agrees on a few tasks relating to potential process improvements identified during a previous [retrospective](#Retrospective) to complete during the sprint.

The tasks are represented on the **sprint board** with either a Post-it per task, or may be split down in the same way as user stories. There is a lane on the **sprint board** used to track the completion of the retrospective-related tasks.

##### Other Tasks

- Two team members are selected to spend a portion of their time [learning](#Learning)
- One member of the team is selected for each week of the sprint to be on [support](#Support)

#### During the Sprint

##### The Sprint Board

During the sprint, the team's progress on the tasks generated during the sprint kick-off is tracked using Post-it notes on a [large physical whiteboard](#sprint-board). This gives the entire team visibility of sprint progress at all times.

![The Corsham Science development team sprint board (captured mid-sprint)](/images/sprint-board.jpeg "The sprint board (captured mid-sprint)")

Columns named ‘to do’, ‘doing’, ‘verify’, and ‘done’ occupy most of the sprint board. The team uses these to track the progress of work during a sprint.

Tasks belonging to stories are represented by Post-its on the board. Each story's task Post-its are grouped into horizontal lanes signified by a title card on the far left.
The Post-its are moved through the columns on the board as they are worked on during the sprint. By the end of a sprint, all of the task Post-its should have migrated from the ‘To do’ column through the ‘Doing’ and ‘Verify’ columns to the ‘Done’ column.

When starting a task, a team member takes the single task Post-it, adds their initials, and places it in the ‘doing’ column. When the work is complete, the task gets moved to the ‘verify’ column, and the team member begins the next task.

Tasks remain in the verify column until the code has been reviewed by another team member based on the [definition of done](docs/definition-of-done.md). Sometimes it is possible to review a single task, but in practice, an entire story may be reviewed as a whole. If changes are requested as part of the review, these should be recorded onto new Post-its and placed in the ‘to do’ column. Once the review process is completed, the story's task Post-its can be moved to the ‘done’ column.

Stories that were deemed too small to be broken down into fine-grained tasks get grouped into a ‘Single Card Stories’ lane near the top of the board.

To minimise the quantity of partially complete stories at the end of a sprint, a [limit](docs/work-in-progress-limit.md) is imposed on the number of 'work in progress stories' (the number of stories currently being worked on). Currently, this limit is set at 3 stories however this is not a fixed limit and may be raised (or lowered) based on sprint composition. The 'work in progress limit' encourages members of the team to work on stories together. Even when the team is not working at the limit, before starting to work on a new story, team members should consider helping to complete a story which is still in progress.

In addition to user stories, the sprint board is also used to track [retrospective goals](#Retrospective-Goals), [tech improvements](#Tech-Improvements), [support tickets](#support) and [distractions](#distractions).

##### Daily Scrums

On each day of a sprint (excluding the first and last), at 1:30 pm, the team gathers around the sprint board for a meeting called the ‘daily scrum.’ Every team member who can stand should do so; this helps to encourage brevity. During the daily scrum each team member answers the following three questions:

- What did you do since the last meeting to help the team finish the Sprint?
- What do you plan to do before the next meeting to help the team finish the Sprint?
- What obstacles are getting in the team's way?

The daily scrum meeting should not be used as a problem-solving or issue resolution meeting. Issues that are raised are usually dealt with immediately after the meeting.

##### Backlog Refinement

To ensure that there are always enough sufficiently specified **user stories** to work on in future sprints, the team must allocate some time during each sprint to maintaining the backlog of work.

Every week, the team has a scheduled meeting to discuss, review, write and estimate **user stories**. During this meeting the businesses priorities should be kept in mind to ensure the correct stories available to be worked on during upcoming sprints.

##### Support

When a team member is allocated to support, it is their responsibility to track and respond to [support tickets](#Freshservice) as they arrive, and to triage tickets onto [the sprint board](#The-Sprint-Board) where appropriate. The member of the team will write up new tickets on Post-its, then place them on the board as a [distraction](#distractions). Like other tasks, they will be moved across the board as they are completed.

##### Learning

During the sprint, any member of the team allocated to learning should spend a portion of their time (currently 20%) on self-improvement. This should be focused on technologies/tools/techniques which could be of benefit to the team in future. Team members have access to the company Pluralsight subscription which provides an array of video training courses but are also free to use other resources that may be relevant.

##### Distractions

A distraction is anything that prevents a team member from spending time on planned sprint tasks, e.g. time spent in meetings or responding to support tickets.

These are recorded on Post-it notes with a description and a rough estimate of time spent on them. Distraction Post-its are normally placed in the rightmost column of the board, however, if an ongoing distraction is taking a long time to resolve, the Post-it may be placed in the doing column of the board.

#### End of Sprint

##### Demos

On the last day of a sprint, the team hosts a demo session to show what has been accomplished during the sprint. This is an open session that can be attended by any interested party, ideally at least one representative from each business department should attend.

The demo is an opportunity for the business to provide feedback on the work done, as well as to facilitate a discussion in the steps required to get these changes into production (such as validation, updating SOPs and user training).

Any issues that are identified during the demo should be added into the idea backlog, so that they can be corrected in a future sprint. This may be either as a user story, or a bug, depending on the nature of the issue.

##### Retrospective

After the demo, the team has a retrospective meeting. During the retrospective, the team discusses how the sprint went, reflecting on what went well during the sprint, any issues that came up, and how productive the sprint was.

The primary objective of these meetings is to identify improvements that could be made to the development process. This is done by reviewing the discussion points added to the [retrospective board](docs/trello.md#Retrospective-Board) during the sprint, as well as any other topics that a member of the team wishes to discuss.

As a result of these discussions, a number of actionable tasks may be discovered, these should be added to the [retrospective board](docs/trello.md#Retrospective-Board) as a potential future process improvement.

An example of a process improvement derived from a retrospective meeting is [the work in progress limit](work-in-progress-limit.md).

Also during the retrospective, the distractions recorded during the sprint are reviewed. The team attempts to identify groups of distractions that could be reduced with software or process improvements (for example, when a few distractions are caused by the same, or similar, recurring issues). This can lead to cards being added to a Trello board to prompt future action.

Members of the team take it in turns to bring snacks for the whole team to this meeting.

##### Time Tracking

At the end of every sprint, each member of the team records how much time they spent working on projects for different customers in a 'Time Breakdowns' Google sheet. The amount of time each team member was absent from work is also recorded on this spreadsheet. This data is used to proportionately bill customers for the team's time.

This is done as a percentage of the users time over the 2 week period, to a granularity of 1/2 a day (5% of the sprint).

##### Tracking the productivity of the sprint

The team maintains a 'Sprint Velocity' Google sheet. Every sprint, various metrics such as 'points achieved', 'total distractions (hours)' etc. are recorded on the spreadsheet. This data is used to track the team's performance (or 'velocity') over time.

The 'notes' section of this spreadsheet is used to record anything that may impact a future sprint, such as team member absences.

## Tools

### Planning Poker Cards

During [estimation](#estimating-effort) sessions, planning poker cards containing Fibonacci numbers (1–21) are used to allow team members to choose, and then simultaneously reveal their estimates. Six-player decks can be purchased from [Agile Stationary](https://agilestationery.co.uk/products/estimation-poker-cards) using the discount code `THANKYOU` to receive 20% off.

### Sprint Board

The board is from Clarus (https://www.clarus.com/gb/products/).

We use magnetic column headers (these are nearly the same as ours - https://www.patboard.com/shop/scrum-magnets-columncards/).

Marking tape is used to separate the board's columns (https://agilestationery.co.uk/products/whiteboard-marking-tape-3mm-black).

### Post-its

We use 'super sticky' Post-its for tasks, stories and distractions:

- [76 x 76 mm](https://www.amazon.co.uk/Post-Notes-Super-Sticky-Value/dp/B00RCJWSE8/)
- [76 x 127 mm](https://www.amazon.co.uk/Post-Notes-Energetic-Colours-extra/dp/B005IXGAWQ/)

### Trello

See [trello.md](docs/trello.md).

### Slack

[Slack](https://slack.com) is used by the development team as a communication tool. This allows direct person-to-person communication, as well as channels dedicated to a particular topic which can be joined by many team members.

The `#general` channel exists by default and can be used for general team discussions and announcements.

Channels regarding a particular project are prefixed with `proj`, for example, `#proj-order-manager`.

Temporary channels for ad-hoc discussions are prefixed with `temp`, for example, `#temp-balances`.

Some channels are used with third-party integrations to provide notifications. These are prefixed with `bot`, for example, `#bot-monitoring`.

### TeamCity

[TeamCity](https://www.jetbrains.com/teamcity/) is a Java-based build management and continuous integration server from JetBrains.

Each Corsham Science project has a corresponding configuration in TeamCity created at the outset. When code is committed to the Git repository, it is automatically built and tested by the TeamCity server. The resulting packages are published to a NuGet feed, to be consumed by [Octopus Deploy](#octopus-deploy).

The build status is automatically pushed back as a status check on the Github pull request. This prevents any change from being merged if it does not build and pass all automated tests.

### Octopus Deploy

[Octopus deploy](https://octopus.com) is a deployment automation server designed to make it easy to orchestrate releases and deploy applications, whether on-premises or in the cloud.

Each Corsham Science project will have a corresponding project in octopus deploy. The project will contain a definition of the deployment workflow, usually deploying one or more packages from the TeamCity NuGet feed.

Each project may also have some variables defined. Upon deployment, Octopus is capable of replacing placeholder values in config files with the appropriate value for the environment into which the software is being deployed (Test, Production, etc.).

For software which is deployed to multiple customers, Octopus supports the concept of ‘Tenants.’ This allows, for example, Bath ASU and Pharmaxo to receive the same system, deployed to separate servers and with bespoke configuration variables.

### 1Password

[1Password](https://1password.com) is the password manager the team uses to store and share work-related passwords securely.

Team members use private vaults to manage passwords for their work-related accounts.

There are also customer-specific vaults. These are used for managing shared credentials associated with a specific customer, or a software system used by that customer.

If a team member needs to use the credentials of a shared account, they can find them in the relevant vault.

## Ceremony Agenda

- [Sprint Kick-off](/docs/ceremony-agenda/sprint-kick-off.md)
- [Daily scrum](/docs/ceremony-agenda/daily-scrum.md)
- [Backlog refinement](/docs/ceremony-agenda/backlog-refinement.md)
- [Demo](/docs/ceremony-agenda/demo.md)
- [Retrospective](/docs/ceremony-agenda/retrospective.md)

## Guidelines

### Design

### Development

- [Source Control](docs/source-control.md)

#### Code Style

- [JavaScript](docs/code-style/javascript.md)
- [C#](docs/code-style/csharp.md)
