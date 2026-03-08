# On-Chain DAO Governance

This repository contains a full suite of smart contracts for decentralized governance. It utilizes the OpenZeppelin Governor standard to provide a secure, modular, and battle-tested framework for community-led decision-making.

## Governance Workflow
1. **Proposal**: A token holder submits a proposal (e.g., "Transfer 10 ETH to the Treasury").
2. **Voting**: Community members cast votes weighted by their token balance.
3. **Queueing**: Once passed, the proposal enters a "Timelock" to allow users to exit if they disagree with the decision.
4. **Execution**: After the timelock expires, anyone can trigger the execution of the proposal's instructions.



## Key Features
* **ERC20Votes Integration**: Snapshot-based voting power to prevent double-spending votes.
* **Timelock Controller**: Prevents "governance attacks" by adding a delay to all executions.
* **Configurable Parameters**: Easily adjust voting delays, periods, and quorum requirements.

## Deployment
1. Deploy `GovernanceToken.sol`.
2. Deploy `TimeLock.sol`.
3. Deploy `GovernorContract.sol` using the addresses of the token and timelock.

## License
MIT
