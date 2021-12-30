---
description: Solidity Documentation For Candle Governor Contract
---

# CandleGovernor Raw

#### CandleGovernor

\
Contract Address - 0xB80Be29667021AE0B617AC9eFe0a3A1a58033681

**Functions**

***

**constructor**

| Name    | Type    | Description |
| ------- | ------- | ----------- |
| \_token | address |             |

Returns:

No parameters

***

**BALLOT\_TYPEHASH**

No parameters

Returns:

| Name | Type    | Description |
| ---- | ------- | ----------- |
|      | bytes32 |             |

***

**COUNTING\_MODE**

See {IGovernor-COUNTING\_MODE}.

No parameters

Returns:

| Name | Type   | Description |
| ---- | ------ | ----------- |
|      | string |             |

***

**castVote**

See {IGovernor-castVote}.

| Name       | Type    | Description |
| ---------- | ------- | ----------- |
| proposalId | uint256 |             |
| support    | uint8   |             |

Returns:

| Name | Type    | Description |
| ---- | ------- | ----------- |
|      | uint256 |             |

***

**castVoteBySig**

See {IGovernor-castVoteBySig}.

| Name       | Type    | Description |
| ---------- | ------- | ----------- |
| proposalId | uint256 |             |
| support    | uint8   |             |
| v          | uint8   |             |
| r          | bytes32 |             |
| s          | bytes32 |             |

Returns:

| Name | Type    | Description |
| ---- | ------- | ----------- |
|      | uint256 |             |

***

**castVoteWithReason**

See {IGovernor-castVoteWithReason}.

| Name       | Type    | Description |
| ---------- | ------- | ----------- |
| proposalId | uint256 |             |
| support    | uint8   |             |
| reason     | string  |             |

Returns:

| Name | Type    | Description |
| ---- | ------- | ----------- |
|      | uint256 |             |

***

**execute**

See {IGovernor-execute}.

| Name            | Type       | Description |
| --------------- | ---------- | ----------- |
| targets         | address\[] |             |
| values          | uint256\[] |             |
| calldatas       | bytes\[]   |             |
| descriptionHash | bytes32    |             |

Returns:

| Name | Type    | Description |
| ---- | ------- | ----------- |
|      | uint256 |             |

***

**getVotes**

We plan to integrate with tally, among other services, to offer a more intuitive governance dashboard.

| Name        | Type    | Description |
| ----------- | ------- | ----------- |
| account     | address |             |
| blockNumber | uint256 |             |

Returns:

| Name | Type    | Description |
| ---- | ------- | ----------- |
|      | uint256 |             |

***

**hasVoted**

See {IGovernor-hasVoted}.

| Name       | Type    | Description |
| ---------- | ------- | ----------- |
| proposalId | uint256 |             |
| account    | address |             |

Returns:

| Name | Type | Description |
| ---- | ---- | ----------- |
|      | bool |             |

***

**hashProposal**

See {IGovernor-hashProposal}. The proposal id is produced by hashing the RLC encoded \`targets\` array, the \`values\` array, the \`calldatas\` array and the descriptionHash (bytes32 which itself is the keccak256 hash of the description string). This proposal id can be produced from the proposal data which is part of the {ProposalCreated} event. It can even be computed in advance, before the proposal is submitted. Note that the chainId and the governor address are not part of the proposal id computation. Consequently, the same proposal (with same operation and same description) will have the same id if submitted on multiple governors accross multiple networks. This also means that in order to execute the same operation twice (on the same governor) the proposer will have to change the description in order to avoid proposal id conflicts.

| Name            | Type       | Description |
| --------------- | ---------- | ----------- |
| targets         | address\[] |             |
| values          | uint256\[] |             |
| calldatas       | bytes\[]   |             |
| descriptionHash | bytes32    |             |

Returns:

| Name | Type    | Description |
| ---- | ------- | ----------- |
|      | uint256 |             |

***

**name**

See {IGovernor-name}.

No parameters

Returns:

| Name | Type   | Description |
| ---- | ------ | ----------- |
|      | string |             |

***

**proposalDeadline**

See {IGovernor-proposalDeadline}.

| Name       | Type    | Description |
| ---------- | ------- | ----------- |
| proposalId | uint256 |             |

Returns:

| Name | Type    | Description |
| ---- | ------- | ----------- |
|      | uint256 |             |

***

**proposalSnapshot**

See {IGovernor-proposalSnapshot}.

| Name       | Type    | Description |
| ---------- | ------- | ----------- |
| proposalId | uint256 |             |

Returns:

| Name | Type    | Description |
| ---- | ------- | ----------- |
|      | uint256 |             |

***

**proposalThreshold**

**The Threshold is set at 20,000,000 CNDL.**

No parameters

Returns:

| Name | Type    | Description |
| ---- | ------- | ----------- |
|      | uint256 |             |

***

**proposalVotes**

Accessor to the internal vote counts.

| Name       | Type    | Description |
| ---------- | ------- | ----------- |
| proposalId | uint256 |             |

Returns:

| Name         | Type    | Description |
| ------------ | ------- | ----------- |
| againstVotes | uint256 |             |
| forVotes     | uint256 |             |
| abstainVotes | uint256 |             |

***

**propose**

See {IGovernor-propose}.

| Name        | Type       | Description |
| ----------- | ---------- | ----------- |
| targets     | address\[] |             |
| values      | uint256\[] |             |
| calldatas   | bytes\[]   |             |
| description | string     |             |

Returns:

| Name | Type    | Description |
| ---- | ------- | ----------- |
|      | uint256 |             |

***

**quorum**

Quorum is achieved with 4% of total CNDL.

| Name        | Type    | Description |
| ----------- | ------- | ----------- |
| blockNumber | uint256 |             |

Returns:

| Name | Type    | Description |
| ---- | ------- | ----------- |
|      | uint256 |             |

***

**quorumDenominator**

**CNDL**

No parameters

Returns:

| Name | Type    | Description |
| ---- | ------- | ----------- |
|      | uint256 |             |

***

**quorumNumerator**

****

No parameters

Returns:

| Name | Type    | Description |
| ---- | ------- | ----------- |
|      | uint256 |             |

***

**setProposalThreshold**

Update the proposal threshold. This operation can only be performed through a governance proposal. Emits a {ProposalThresholdSet} event.

| Name                 | Type    | Description |
| -------------------- | ------- | ----------- |
| newProposalThreshold | uint256 |             |

Returns:

No parameters

***

**setVotingDelay**

Update the voting delay. This operation can only be performed through a governance proposal. Emits a {VotingDelaySet} event.

| Name           | Type    | Description |
| -------------- | ------- | ----------- |
| newVotingDelay | uint256 |             |

Returns:

No parameters

***

**setVotingPeriod**

Update the voting period. This operation can only be performed through a governance proposal. Emits a {VotingPeriodSet} event.

| Name            | Type    | Description |
| --------------- | ------- | ----------- |
| newVotingPeriod | uint256 |             |

Returns:

No parameters

***

**state**

See {IGovernor-state}.

| Name       | Type    | Description |
| ---------- | ------- | ----------- |
| proposalId | uint256 |             |

Returns:

| Name | Type  | Description |
| ---- | ----- | ----------- |
|      | uint8 |             |

***

**supportsInterface**

See {IERC165-supportsInterface}.

| Name        | Type   | Description |
| ----------- | ------ | ----------- |
| interfaceId | bytes4 |             |

Returns:

| Name | Type | Description |
| ---- | ---- | ----------- |
|      | bool |             |

***

**token**

**CNDL, the token used to allocate votes and integrate with the CandleGovernor Contract**

No parameters

Returns:

| Name | Type    | Description |
| ---- | ------- | ----------- |
|      | address |             |

***

**updateQuorumNumerator**

****

| Name               | Type    | Description |
| ------------------ | ------- | ----------- |
| newQuorumNumerator | uint256 |             |

Returns:

No parameters

***

**version**

See {IGovernor-version}.

No parameters

Returns:

| Name | Type   | Description |
| ---- | ------ | ----------- |
|      | string |             |

***

**votingDelay**

****

No parameters

Returns:

| Name | Type    | Description |
| ---- | ------- | ----------- |
|      | uint256 |             |

***

**votingPeriod**

****

No parameters

Returns:

| Name | Type    | Description |
| ---- | ------- | ----------- |
|      | uint256 |             |

***

****

****





