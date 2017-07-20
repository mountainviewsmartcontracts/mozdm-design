# Product Manager

The product manager in this system is the hands-on manager of the software product - they configure or otherwise control the issue tracker, and other software management systems.

## Adjusting the Reward Algorithm (we've also been calling this a Payout Algorithm)

A reward algorithm kicks in when an market contract has been resolved.

Typically, contract resolution results in some payment being made. That payment could be made immediately, or in installments, or based on other conditions being met, such as code quality being verified, or other metrics.  

One way we could make it easy to adjust the Reward Algorithm is to create a domain specific language (DSL) for defining the algorithm.

We've been calling this potential DSL, used to define the Reward/Payout algorithm a "Payout DSL"

The Payout DSL is TBD.

Use Cases for the Product Manager:

- Create Payout Algorithm
- Backtest Payout
- Publish Payout
- Retire Payout

Publishing payment terms might be restricted - Product owner or Industry Partner.

## Repo Management

Note: anybody can browse/add/view any repo.

### Browsing the Repo List

![browse](/img/_RepoList.png)

### Adding a Repo

![add](/img/_RepoAdd.png)

### Showing Repo Details

![add](/img/_RepoDetails.png)

1) Only show the delete button if there are no open contracts.  Auto-delete a repo if there have been no open contracts for 30 days.

