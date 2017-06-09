# Elements

![Entities](/img/__Overview.png)

## Contracts

### Types

Issue Market trades two types of contracts:

- a **Reward** <br/>
  eg `I will pay $X if Issue $Y is resolved before $Date`

- a **Forecast** <br/>
  eg `I will pay $X if an Issue with ${MATCH PARAMS} is opened before $DATE`

### Payout Algorithm

- We will create a DSL for pluggable payout algorithms
- Each contract is associated with one (and only one) payout algorithm

## Repos 

### Types

*Repo Types* are hard coded into the system.

| REPO TYPE | SUPPORTED CONTRACT TYPES |
|-----------|--------------------------|
| GitHub    | BOUNTY, FORECAST         |
| BugZilla  | BOUNTY, FORECAST         |
| CVE       | FORECAST                 |

### Characteristics

- Some repos are hard-coded in the system (BugZilla/Firefox,
  BugZilla/Thunderbird, CVE)
- Some repos are added dynamically by users (GitHub/Repo1, GitHub/Repo2, ...)

## Issues

### Attributes

Note: For each issue we can programatically extract:

- the issue status (Open, Closed)
- the issue metadata

| REPO TYPE | ISSUE META-DATA                       |
|-----------|---------------------------------------|
| CVE       | [hardcoded] severity, type, etc. etc. |
| BugZilla  | [hardcoded] severity, etc.            |
| GitHub    | [dynamic] labels                      |

### Sync

We pull issues from each repo periodicaly (once an hour?) and resolve in the
oracle.

### Match Params

- **CVE** - match against issue metadata
- **BUGZILLA** - match against issue metadata
- **GitHub** - match against issue labels

