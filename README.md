# Token Contract 

This README provides an overview of the `Token` contract, a Solidity smart contract developed for managing a custom ERC-20 token named "Degen" (symbol: DGN). The contract includes functionalities for minting, transferring, burning tokens, redeeming game rewards, and granting bonus tokens.

## Overview

The `Token` contract is built upon the ERC-20 standard and extends functionality using OpenZeppelin's contracts, including `Ownable` for access control and `ERC20Burnable` for token burning capabilities.

## Features

### Minting Tokens

The contract allows the owner to mint new tokens and assign them to a specified address.

```solidity
function mintTokens(address grantee, uint256 mass) external onlyOwner
```

### Transferring Tokens

Owners or users can transfer tokens to other addresses.

```solidity
function transferTokens(address grantee, uint256 mass) external
```

### Burning Tokens

Tokens can be burned by the owner.

```solidity
function burn(uint256 mass) public override
```

### Redeeming Game Rewards

Users can redeem game rewards by burning a specific amount of tokens corresponding to the reward's cost.

```solidity
function redeemGameReward(GameReward gameReward) external
```

### Checking Player Balance

Users can check their token balance.

```solidity
function getPlayerBalance(address player) external view returns (uint256)
```

### Granting Bonus Tokens

The owner can grant bonus tokens to a specified address.

```solidity
function grantBonusTokens(address grantee, uint256 mass) external onlyOwner
```

## Game Rewards

The contract includes an enumeration `GameReward` with predefined rewards such as Gold Coins, Magic Scroll, and Enchanted Gem. Each reward has an associated cost in tokens.

## Initialization

The contract is initialized with an initial supply of 100 tokens, distributed to the contract deployer.

## Dependencies

The contract utilizes OpenZeppelin's ERC-20, Ownable, and ERC20Burnable contracts. Make sure to include these dependencies when deploying the contract.

## License

This contract is released under the MIT License.

## Author

Prathap Singh

p19982102@gmail.com
