# WETH9 - Wrapped Ether for Jovay

This repository contains the WETH9 (Wrapped Ether) contract implementation for Jovay network.

## Overview

WETH9 is a canonical ERC20-compatible wrapper for native Ether, enabling ETH to be used in DeFi protocols and smart contracts that require ERC20 token standards. This implementation follows the battle-tested WETH9 contract pattern originally deployed on Ethereum mainnet.

## Contract Addresses

- **Jovay Mainnet**: *Coming soon*
- **Jovay Testnet**: `0xFe06d41BA962A74209845f938c387b363a931505`

## Features

- **ERC20 Compatible**: Standard ERC20 token interface with 18 decimal places
- **1:1 Peg**: Each WETH token is backed 1:1 by native ETH
- **Gas Efficient**: Optimized for minimal gas consumption
- **Battle Tested**: Based on the proven WETH9 implementation from Ethereum mainnet

## Core Functions

- `deposit()`: Wrap ETH to receive WETH tokens
- `withdraw(uint wad)`: Unwrap WETH to receive ETH
- `transfer(address dst, uint wad)`: Transfer WETH tokens
- `approve(address guy, uint wad)`: Approve spending allowance

## Compilation

### Prerequisites
```bash
npm install -g solc@0.4.18
```

### Compile Contract
```bash
npx solc@0.4.18 --bin --abi --optimize -o ./artifacts contracts/WETH9.sol
```

## Contract Details

- **Solidity Version**: ^0.4.18
- **Token Name**: Wrapped Ether
- **Token Symbol**: WETH
- **Decimals**: 18

## Usage

Users can wrap ETH by sending it to the contract (which automatically calls `deposit()`) or by calling the `deposit()` function directly. WETH can be unwrapped back to ETH using the `withdraw()` function.

## Security

This implementation is based on the original WETH9 contract that has been extensively audited and battle-tested on Ethereum mainnet.
