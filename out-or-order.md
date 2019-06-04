### Prioritisation

The business intermittently advises the team on their current short-term and long-term goals.

At the start of a sprint, the team tries to pick stories relating to the business’ current priorities to include in the sprint.

Priorities are also essential to keep in mind during **backlog refinement** meetings.

It is more important for the team to specify and estimate stories relating to the business’ urgent priorities than reviewing more general feature requests.

##### Tracking the productivity of different sprints

The team maintains a 'Sprint Velocity' Google sheet. Every sprint, various metrics such as 'points achieved', 'total distractions (hours)' etc. are recorded on the spreadsheet. This data is used to track the team's performance (or 'velocity') over time.
The 'notes' section of this spreadsheet is used to record team members' planned leave from work.

#### Definition of Done

It is essential to have a well defined ‘definition of done’ so that we know when we should call a story complete. This effectively forms an implicit set of acceptance criteria which is applied to every story. Our definition of done is expected to evolve. Currently, it includes the following criteria:

- Working code has been produced which satisfies all acceptance criteria listed on the Trello card.
- All code conforms to our chosen style for the relevant language. This rule is relaxed for projects which have not yet been fully converted to conform with our style guide.
- Documentation has been produced.
  - All projects should have a set of release notes in the PR comment. They should describe any new functionality as well as a technical description of any configuration or infrastructure changes required to deploy it.
  - For projects which are formally documented, the documentation should be reviewed and updated where appropriate.
- Unit tests have been written where appropriate, and all existing tests are passing.
- Manual testing has been performed to ensure that the feature works as expected.
- The working change has been demonstrated to the rest of the team.
- The automated TeamCity build for the project is succeeding.
- A pull request has been submitted to the appropriate repository and reviewed by at least one other member of the team.
- Any required configuration or process changes have been made in Octopus Deploy so that the change could be deployed with no additional work.

#### Backlog Refinement

To ensure that there are always enough sufficiently specified **user stories** to work on in future sprints, the team must allocate some time during each sprint to maintaining the backlog of work.

Every Tuesday afternoon, the team has a meeting to discuss, review, write and estimate **user stories**. These meetings are called backlog refinement meetings.