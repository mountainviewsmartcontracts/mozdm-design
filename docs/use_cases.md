# Use Cases

| Actor           | Organization | Overview                            |
|-----------------|--------------|-------------------------------------|
| Product Manager | Any          | Manages Payout Algorithms           |
| Developer       | Any          | Watches Market, Fixes Bugs          |
| Product Owner   | Mozilla      | Assembles and Watches Metrics       |
| Publisher       | Any          | Configures/Publishes a new contract |
| Counterparty    | Any          | Takes a contract                    |

## Product Manager

| Prioritization Use Case             | Description       |
|-------------------------------------|-------------------|
| [create an account][create_account] | Create an account |
| [create payout][create_payout]      | Create payout     |
| [backtest payout][backtest_payout]  | Create payout     |
| [retire payout][retire_payout]      | Retire payout     |

[create_account]:  cases/all_roles/#create-an-account
[create_payout]:   cases/product_manager/#create-an-account
[backtest_payout]: cases/product_manager/#create-an-account
[retire_payout]:   cases/product_manager/#create-an-account

## Developer

- creates an account
- accepts challenge
- fixes bugs

## Product Owner

- creates an account
- collects metrics

## Contract Publisher

- creats an account
- creates prediction

## Contract Counterparty

- searches for contracts
- takes a contract

