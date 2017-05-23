# System Overview

![Entities](/img/__Overview.png)

## Contracts

### Types

The system supports two types of contracts:

- a **Bounty** <br/>
  eg `I will pay $X if Issue $Y is resolved before $Date`

- a **Prediction** <br/>
  eg `I will pay $X if an Issue with ${MATCH PARAMS} is opened before $DATE`

### Payout Algorithm

- We will create a DSL for pluggable payout algorithms
- Each contract is associated with one (and only one) payout algorithm

## Repos 

Initially, we will support github issues.

### Types

A collection of *Repo Types* are hard coded into the system.

| REPO TYPE | SUPPORTED CONTRACT TYPES |
|-----------|--------------------------|
| GitHub    | BOUNTY, PREDICTION       |
| BugZilla  | BOUNTY, PREDICTION       |
| CVE       | PREDICTION               |

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

## Questions

- are the CONTRACT TYPES correct - are there only two??
- what is the best vocabulary to use?
- what is the right language to describe the CONTRACT TYPES??
- what happens if params change during the contract period?
