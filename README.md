# SimpleDAO

SimpleDAO is a decentralized autonomous organization (DAO) built on the Scroll blockchain. This project allows members to join the DAO, create proposals, and vote on them.

## Key Features

- **Membership**:
  - Join the DAO by paying a membership fee (1 ether).
  - Track members using a mapping.

- **Proposal Creation**:
  - Create proposals with a description and voting deadline.
  - Store proposal details.

- **Voting**:
  - Vote on proposals (e.g., "yes" or "no").
  - Tally votes and determine if a proposal passes based on a quorum.

## Smart Contract Overview

### Structs

- **Proposal**: 
  - `description` (string): The description of the proposal.
  - `deadline` (uint256): The voting deadline for the proposal.
  - `yesVotes` (uint256): The number of "yes" votes.
  - `noVotes` (uint256): The number of "no" votes.
  - `executed` (bool): Whether the proposal has been executed.

### Enums

- **DepositStatus**: 
  - `Pending`: The deposit is awaiting approval.
  - `Approved`: The deposit has been approved.
  - `Rejected`: The deposit has been rejected.

### Functions

- **Membership**:
  - `joinDAO()`: Join the DAO by paying a membership fee.
  - `createProposal(string memory _description, uint256 _votingPeriod)`: Create a new proposal.
  - `vote(uint256 proposalId, bool support)`: Vote on a proposal.
  - `executeProposal(uint256 proposalId)`: Execute a proposal if it has passed.
  - `getProposals()`: Get the list of all proposals.

## Deployment

This contract has been deployed on the Scroll Sepolia testnet. The contract address is:

`0x25781e83572aC6fD4068f0d3bacF805d32119630`

## Usage

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/umutkarakas34/SimpleDAO.git
    cd SimpleDAO
    ```

2. **Compile and Deploy**:
    - Use Remix IDE or any Ethereum development framework like Truffle or Hardhat to compile and deploy the contract.

3. **Interact with the Contract**:
    - Use the provided functions to join the DAO, create proposals, and vote. Make sure to use an account with membership for restricted functions.

## License

This project is licensed under the MIT License.

