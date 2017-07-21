# Elements

## Contracts

BugMark trades **Reward Contacts** and a **Forecast Contracts**.

### Forecast Contract

`"I will pay $X if an Issue matching ${METADATA} exists before $DATE"`

![Entities](/img/__OverviewForecast.png)
                                                    
### Reward Contact

`"I will pay $X if Issue $Y is resolved before $Date"`

![Entities](/img/__OverviewReward.png)

### Contract Attributes

| ATTRIBUTE        | DESCRIPTION                               |
|------------------|-------------------------------------------|
| Premium          | Adjustable risk premium                   |
| Metadata         | Labels and Fields used for issue matching |
| Payout Algorithm | DSL for pluggable payout algorithm        |

## Repos 

### Types

*Repo Types* are hard coded into the system.

| REPO TYPE | SUPPORTED CONTRACT TYPES |
|-----------|--------------------------|
| GitHub    | REWARD, FORECAST         |
| BugZilla  | REWARD, FORECAST         |
| CVE       | FORECAST                 |

### Characteristics

- Some repos are hard-coded in the system (eg BugZilla/Firefox,
  BugZilla/Thunderbird, CVE)
- Some repos are added dynamically by users (eg GitHub/Repo1, GitHub/Repo2, ...)

## Issues

### Issue Metadata

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

- **CVE** - match against hardcoded metadata fields
- **BUGZILLA** - match against hardcoded metadata fields
- **GitHub** - match against dynamic labels

