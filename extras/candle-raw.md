---
description: Raw Smart Contract Documentation
---

# Candle Raw

ERC20 Address: 0xbc138bD20C98186CC0342C8e380953aF0cb48BA8
### **Functions**

**constructor**

No parameters

Returns:

No parameters

***

**DOMAIN\_SEPARATOR**

See {IERC20Permit-DOMAIN\_SEPARATOR}.

No parameters

Returns:

| Name | Type    | Description |
| ---- | ------- | ----------- |
|      | bytes32 |             |

***

**allowance**

See {IERC20-allowance}.

| Name    | Type    | Description |
| ------- | ------- | ----------- |
| owner   | address |             |
| spender | address |             |

Returns:

| Name | Type    | Description |
| ---- | ------- | ----------- |
|      | uint256 |             |

***

**approve**

See {IERC20-approve}. Requirements: - \`spender\` cannot be the zero address.

| Name    | Type    | Description |
| ------- | ------- | ----------- |
| spender | address |             |
| amount  | uint256 |             |

Returns:

| Name | Type | Description |
| ---- | ---- | ----------- |
|      | bool |             |

***

**balanceOf**

See {IERC20-balanceOf}.

| Name    | Type    | Description |
| ------- | ------- | ----------- |
| account | address |             |

Returns:

| Name | Type    | Description |
| ---- | ------- | ----------- |
|      | uint256 |             |

***

**burn**

Destroys \`amount\` tokens from the caller. See {ERC20-\_burn}.

| Name   | Type    | Description |
| ------ | ------- | ----------- |
| amount | uint256 |             |

Returns:

No parameters

***

**burnFrom**

Destroys \`amount\` tokens from \`account\`, deducting from the caller's allowance. See {ERC20-\_burn} and {ERC20-allowance}. Requirements: - the caller must have allowance for \`\`accounts\`\`'s tokens of at least \`amount\`.

| Name    | Type    | Description |
| ------- | ------- | ----------- |
| account | address |             |
| amount  | uint256 |             |

Returns:

No parameters

***

**checkpoints**

Get the \`pos\`-th checkpoint for \`account\`.

| Name    | Type    | Description |
| ------- | ------- | ----------- |
| account | address |             |
| pos     | uint32  |             |

Returns:

| Name | Type  | Description |
| ---- | ----- | ----------- |
|      | tuple |             |

***

**decimals**

Returns the number of decimals used to get its user representation. For example, if \`decimals\` equals \`2\`, a balance of \`505\` tokens should be displayed to a user as \`5.05\` (\`505 / 10 \*\* 2\`). Tokens usually opt for a value of 18, imitating the relationship between Ether and Wei. This is the value {ERC20} uses, unless this function is overridden; NOTE: This information is only used for \_display\_ purposes: it in no way affects any of the arithmetic of the contract, including {IERC20-balanceOf} and {IERC20-transfer}.

No parameters

Returns:

| Name | Type  | Description |
| ---- | ----- | ----------- |
|      | uint8 |             |

***

**decreaseAllowance**

Atomically decreases the allowance granted to \`spender\` by the caller. This is an alternative to {approve} that can be used as a mitigation for problems described in {IERC20-approve}. Emits an {Approval} event indicating the updated allowance. Requirements: - \`spender\` cannot be the zero address. - \`spender\` must have allowance for the caller of at least \`subtractedValue\`.

| Name            | Type    | Description |
| --------------- | ------- | ----------- |
| spender         | address |             |
| subtractedValue | uint256 |             |

Returns:

| Name | Type | Description |
| ---- | ---- | ----------- |
|      | bool |             |

***

**delegate**

Delegate votes from the sender to \`delegatee\`.

| Name      | Type    | Description |
| --------- | ------- | ----------- |
| delegatee | address |             |

Returns:

No parameters

***

**delegateBySig**

Delegates votes from signer to \`delegatee\`

| Name      | Type    | Description |
| --------- | ------- | ----------- |
| delegatee | address |             |
| nonce     | uint256 |             |
| expiry    | uint256 |             |
| v         | uint8   |             |
| r         | bytes32 |             |
| s         | bytes32 |             |

Returns:

No parameters

***

**delegates**

Get the address \`account\` is currently delegating to.

| Name    | Type    | Description |
| ------- | ------- | ----------- |
| account | address |             |

Returns:

| Name | Type    | Description |
| ---- | ------- | ----------- |
|      | address |             |

***

**flashFee**

Returns the fee applied when doing flash loans. By default this implementation has 0 fees. This function can be overloaded to make the flash loan mechanism deflationary.

| Name   | Type    | Description                        |
| ------ | ------- | ---------------------------------- |
| token  | address | The token to be flash loaned.      |
| amount | uint256 | The amount of tokens to be loaned. |

Returns:

| Name | Type    | Description |
| ---- | ------- | ----------- |
|      | uint256 |             |

***

**flashLoan**

Performs a flash loan. New tokens are minted and sent to the \`receiver\`, who is required to implement the {IERC3156FlashBorrower} interface. By the end of the flash loan, the receiver is expected to own amount + fee tokens and have them approved back to the token contract itself so they can be burned.

| Name     | Type    | Description                                                                                         |
| -------- | ------- | --------------------------------------------------------------------------------------------------- |
| receiver | address | The receiver of the flash loan. Should implement the {IERC3156FlashBorrower.onFlashLoan} interface. |
| token    | address | The token to be flash loaned. Only \`address(this)\` is supported.                                  |
| amount   | uint256 | The amount of tokens to be loaned.                                                                  |
| data     | bytes   | An arbitrary datafield that is passed to the receiver.                                              |

Returns:

| Name | Type | Description |
| ---- | ---- | ----------- |
|      | bool |             |

***

**getPastTotalSupply**

Retrieve the \`totalSupply\` at the end of \`blockNumber\`. Note, this value is the sum of all balances. It is but NOT the sum of all the delegated votes! Requirements: - \`blockNumber\` must have been already mined

| Name        | Type    | Description |
| ----------- | ------- | ----------- |
| blockNumber | uint256 |             |

Returns:

| Name | Type    | Description |
| ---- | ------- | ----------- |
|      | uint256 |             |

***

**getPastVotes**

Retrieve the number of votes for \`account\` at the end of \`blockNumber\`. Requirements: - \`blockNumber\` must have been already mined

| Name        | Type    | Description |
| ----------- | ------- | ----------- |
| account     | address |             |
| blockNumber | uint256 |             |

Returns:

| Name | Type    | Description |
| ---- | ------- | ----------- |
|      | uint256 |             |

***

**getVotes**

Gets the current votes balance for \`account\`

| Name    | Type    | Description |
| ------- | ------- | ----------- |
| account | address |             |

Returns:

| Name | Type    | Description |
| ---- | ------- | ----------- |
|      | uint256 |             |

***

**increaseAllowance**

Atomically increases the allowance granted to \`spender\` by the caller. This is an alternative to {approve} that can be used as a mitigation for problems described in {IERC20-approve}. Emits an {Approval} event indicating the updated allowance. Requirements: - \`spender\` cannot be the zero address.

| Name       | Type    | Description |
| ---------- | ------- | ----------- |
| spender    | address |             |
| addedValue | uint256 |             |

Returns:

| Name | Type | Description |
| ---- | ---- | ----------- |
|      | bool |             |

***

**maxFlashLoan**

Returns the maximum amount of tokens available for loan.

| Name  | Type    | Description                                 |
| ----- | ------- | ------------------------------------------- |
| token | address | The address of the token that is requested. |

Returns:

| Name | Type    | Description |
| ---- | ------- | ----------- |
|      | uint256 |             |

***

**name**

Returns the name of the token.

No parameters

Returns:

| Name | Type   | Description |
| ---- | ------ | ----------- |
|      | string |             |

***

**nonces**

See {IERC20Permit-nonces}.

| Name  | Type    | Description |
| ----- | ------- | ----------- |
| owner | address |             |

Returns:

| Name | Type    | Description |
| ---- | ------- | ----------- |
|      | uint256 |             |

***

**numCheckpoints**

Get number of checkpoints for \`account\`.

| Name    | Type    | Description |
| ------- | ------- | ----------- |
| account | address |             |

Returns:

| Name | Type   | Description |
| ---- | ------ | ----------- |
|      | uint32 |             |

***

**permit**

See {IERC20Permit-permit}.

| Name     | Type    | Description |
| -------- | ------- | ----------- |
| owner    | address |             |
| spender  | address |             |
| value    | uint256 |             |
| deadline | uint256 |             |
| v        | uint8   |             |
| r        | bytes32 |             |
| s        | bytes32 |             |

Returns:

No parameters

***

**symbol**

Returns the symbol of the token, usually a shorter version of the name.

No parameters

Returns:

| Name | Type   | Description |
| ---- | ------ | ----------- |
|      | string |             |

***

**totalSupply**

See {IERC20-totalSupply}.

No parameters

Returns:

| Name | Type    | Description |
| ---- | ------- | ----------- |
|      | uint256 |             |

***

**transfer**

See {IERC20-transfer}. Requirements: - \`recipient\` cannot be the zero address. - the caller must have a balance of at least \`amount\`.

| Name      | Type    | Description |
| --------- | ------- | ----------- |
| recipient | address |             |
| amount    | uint256 |             |

Returns:

| Name | Type | Description |
| ---- | ---- | ----------- |
|      | bool |             |

***

**transferFrom**

See {IERC20-transferFrom}. Emits an {Approval} event indicating the updated allowance. This is not required by the EIP. See the note at the beginning of {ERC20}. Requirements: - \`sender\` and \`recipient\` cannot be the zero address. - \`sender\` must have a balance of at least \`amount\`. - the caller must have allowance for \`\`sender\`\`'s tokens of at least \`amount\`.

| Name      | Type    | Description |
| --------- | ------- | ----------- |
| sender    | address |             |
| recipient | address |             |
| amount    | uint256 |             |

Returns:

| Name | Type | Description |
| ---- | ---- | ----------- |
|      | bool |             |
