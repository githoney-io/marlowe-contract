# marlowe-contract
The Marlowe Smart Contract for Githoney MVP 🍯

The Bounty on-chain contract is implemented using Marlowe, a domain-specific language for financial smart contracts on the Cardano blockchain. Marlowe's design promotes safety by limiting the kinds of contracts that can be written.

To further ensure security, each bounty functions as its own independent contract, often referred to as a peer-to-peer contract. Marlowe contracts provide several guarantees as part of the language design, but having one contract per bounty limits the blast radius of any security issues, which is a very good quality to have.

A Maintainer deposits funds to create a bounty, paying a minor initiation fee to GitHoney. The initiation fee is set at 2 ADA.

After some external criterion is met, the Admin can move the tokens from the Maintainer’s account to the Developer’s account.

If the Admin approves the merge of a pull request, both the Developer who completed the task and GitHoney (for their facilitation) receive their respective payments.

In summary, the contract enables one party (the Maintainer) to make a payment to another party (the Developer) by locking funds in the contract and delegating the responsibility of unlocking the funds to a 3rd party (the Bot).
