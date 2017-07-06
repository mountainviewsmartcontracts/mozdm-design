
# High Level Processes Interaction

*Users* interact with the marked Dapp through firefox or another browse with the metamask plugin installed.  This is how they make predictions, or take a side of a prediction.

The *Oracle* is a cron job that interacts with issue trackers and feeds data on to the blockchain periodically to two smart contracts.

The *Dapp* has a web interface that loads data from the ethereum blockchain.  The *Dapp* also has two smart contracts.

The *Market* smart contract interacts with users through the web3 UI, and checks the blockchain for data on the currrent status of predictions and bugs when the page is loaded.

The *Reward Algorithm* smart contract is fed data by the Oracle about current bug statuses, and calculates payouts for users of the system.

Future stuff not shown: Scoring Algos, Bots.

![Entities](/img/ProcessInteraction.png)

[docs]: https://github.com/mvscorg/mozdm-design
[web2]: https://github.com/mvscorg/mvscim
[web3]: https://github.com/mvscorg/xdmarket


