## Cycles

A cycle is normally two weeks long. They start and end with brief review meetings to review the previous cycle and plan the next.

### Example cycle

- Day 1: Review new feature requests, plan cycle ahead
- Day 1 & 2: Small features
- Day 3–9: Main feature
- Day 10: Documentation, deployment, review

### The *Active Software Development* Trello Board

At the plannning meeting on the first morning of a new cycle, we will decide on a set of tasks which the team will tackle over the next two weeks. These may include non-development activities such as specifying a new feature, or producing documentation.

For each of these tasks, a card will be added to our private trello board named *Active Software Development*. If applicable the card description should contain a link back to the source card on the customer facing `Software Development` board.

During development technical discussions, fine grained todo lists and notes may be added to these cards without polluting the customer card which describes the original requirements.

The board will contain the following lists:

- **Current Cycle** for cards which have been scheduled for the current cycle but where work has not yet started.
- **In Development** for cards which are currently in progress
- **Testing** for cards which have had the majority of their development completed, but require internal testing before being delivered to the customer.
- **Delivered (Cycle -> DD/MM/YY)** for features which have been delivered to customers. A new instance of this list will be created every cycle to keep track of when tasks were completed.
