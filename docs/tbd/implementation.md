# Implementation Scope

The design will accomodate all features. We plan to implement Version 0
features in this project, and Version N features in follow-on efforts.

| Area                 | Version 0                | Version N                                |
|----------------------|--------------------------|------------------------------------------|
| Repo Types           | GitHub Issues            | BugZilla, CVE                            |
| Contract Parties[^1] | One-to-One Contracts     | Multi-Party Contracts                    |
| Payout Algorithm     | One hard-coded algorithm | Pluggable algorithm, Configuration UI    |
| Metrics              | Show Current Status      | Export Data to Health Dash, TimeSeriesDB |

[^1]:
    Note that there can be multiple contracts against a single issue, all
    running in parallel. 

