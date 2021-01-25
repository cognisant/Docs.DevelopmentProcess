# Definition of Done

It is essential to have a well defined ‘definition of done’ so that we know when we should call a story complete. This effectively forms an implicit set of acceptance criteria which is applied to every story. Our definition of done is expected to evolve. Currently, it includes the following criteria:

- Working code has been produced which satisfies all acceptance criteria listed on the Trello card.
- The functionality has been demo'd to other members of the development team.
- All code conforms to our chosen style for the relevant language. This rule is relaxed for projects which have not yet been fully converted to conform with our style guide.
- Documentation has been produced.
  - A test plan should be produced outlining the manual tests to be performed to verify the acceptance criteria. This will have been approved, and then executed by a member of the team, with appropriate evidence being recorded.
  - All projects should have a set of release notes in the PR comment. They should describe any new functionality as well as a technical description of any configuration or infrastructure changes required to deploy it.
  - For projects which are formally documented, the documentation should be reviewed and updated where appropriate.
- Unit tests have been written where appropriate, and all existing tests are passing.
- Manual testing has been performed to ensure that the feature works as expected.
- The working change has been demonstrated to the rest of the team.
- The automated TeamCity build for the project is succeeding.
- A pull request has been submitted to the appropriate repository and reviewed by at least one other member of the team.
- Any required configuration or process changes have been made in Octopus Deploy so that the change could be deployed with no additional work.
