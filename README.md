# Module 3 Types Of Function

This Solidity smart contract, named Module3, extends ERC20 functionality with additional features including ownership management and custom transfer events.

## Overview

The contract includes the following features:

- **ERC20 Token**: Inherits from OpenZeppelin's ERC20 contract to provide standard token functionality.
- **Ownership**: Extends from OpenZeppelin's Ownable contract, allowing for ownership control.
- **Custom Events**: Emits a custom event `TransferCustom` upon successful transfers.
- **Constructor**: Initializes the contract with an initial supply of tokens, token name, and token symbol.

## Functionality

### Constructor

Upon deployment (`constructor`), the contract initializes with:
- An initial supply of tokens (`initialSupply`).
- Token details (`tokenName` and `tokenSymbol`) passed during deployment.
- Ownership assigned to the deployer (`msg.sender`).

### Token Management

- **Transfer**: Overrides ERC20's `transfer` function to emit a custom event (`TransferCustom`) upon successful transfer.
- **TransferFrom**: Overrides ERC20's `transferFrom` function similarly to emit `TransferCustom`.
- **Mint**: Allows the contract owner to mint new tokens to a specified address using the `mint` function.
- **Burn**: Allows any token holder to burn (destroy) a specified amount of their tokens using the `burn` function.

### Modifiers

- **onlyOwner**: Restricts access to functions using the Ownable modifier, ensuring only the contract owner can perform certain operations like minting tokens.

## Usage

1. **Deploying the Contract**: Deploy the contract on a supported Ethereum environment such as Remix IDE (remix.ethereum.org).
2. **Interacting with the Contract**: Use functions like `transfer`, `mint`, `burn`, and other standard ERC20 methods to manage tokens and ownership.

## Development Environment

This contract was developed and tested using Remix IDE (remix.ethereum.org).

## Author

Marielle Romana

NTC EMAIL: 421000169@ntc.edu.ph

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for more details.

