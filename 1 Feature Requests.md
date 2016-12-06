# Managing the backlog of changes

## Gathering Requirements
Our primary means of gathering requirements is the [Feature request form](https://github.com/cognisant/trello-form). This is accessed via a web browser at a url unique to each Cognisant customer. It invites users to provide:

- A description of a problem
* The business impact of their problem, to be used for prioritization
* [Optionally] A suggested solution to that problem

Completing this form will automatically create a card on Trello containing these details. The use of a structured form ensures that the requests we receive have been given an appropriate amount of thought and are in a consistent format.

## The *Software Development* Trello board
Each customer will have their own board on Trello to hold their backlog of change requests.

End users do not have access to modify cards on this board directly but can add comments and subscribe to the card to receive notifications on its progress.

### Trello Card Format

**Titles**

Card titles are edited by the development team throughout the card’s progress to include useful information. They will follow this template:

*Product: Request Title (Time Estimate)*

Time estimates are written as a number of person days (PD), person weeks (PW), team days (TD) or team weeks (TW). For example:

- BMS: Add text message notifications (2 PW)
- Order Manager: Include PS order lines (3 TD)

Card titles may change as the problem and solutions are better understood.

**Descriptions**

Card descriptions will be added to by the development team. To begin with, they will include the description provided by the original author. Once agreed, the development team will write a specification that explains the scope of the work and the steps necessary to complete it.

### Lists

The software development board will contain the following lists. Cards will be moved by the team to reflect their development progress.

- **New Requests** is an inbox fed by the feature request form.
- **On Hold** for cards which cannot be currently worked on but may be in the future.
- **Agreed** for cards that will be worked on.
- **Specified** for cards with a specification written by the development team.
- **In Development** for cards that are being worked on.
- **Ready to Deploy** for cards that are awaiting deployment.
- **Done** for cards that have been completed.
- **Rejected** for cards that will not be worked on.
