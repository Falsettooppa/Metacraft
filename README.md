# Metacraft
A token creation
# MyToken Contract

This Solidity contract defines a simple ERC20 token called MyToken. It allows for the creation of tokens with a fixed supply, as well as minting and burning of tokens by authorized addresses.

## Features

- **Token Details**: The contract stores details about the token, including its name, symbol, and total supply.
- **Token Balances**: It maintains a mapping of addresses to token balances.
- **Minting**: The contract provides a mint function to create new tokens and assign them to a specified address.
- **Burning**: It includes a burn function to destroy tokens held by a specified address.

## Contract Details

- **Name**: MyToken
- **Version**: Solidity ^0.8.0
- **License**: MIT

## Functions

### Constructor

The contract constructor initializes the token details including its name, symbol, and totalSupply. The entire supply is initially allocated to the address deploying the contract.

### mint Function

- *Parameters*: _account (address), _value (uint256)
- *Access Control*: Public
- *Purpose*: Mint new tokens and assign them to the specified address.
- *Requirements*: 
  - The _account address must be valid.
  - The _value parameter must be greater than zero.
- *Effects*: Increases the total supply and the balance of the specified address.

### burn Function

- *Parameters*: _account (address), _value (uint256)
- *Access Control*: Public
- *Purpose*: Destroy tokens held by the specified address.
- *Requirements*: 
  - The _account address must be valid.
  - The _value parameter must be greater than zero.
  - The _account must have sufficient balance to burn the specified amount of tokens.
- *Effects*: Decreases the total supply and the balance of the specified address.

## License

This contract is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.
