# Uniswap Interface

[![Lint](https://github.com/Uniswap/uniswap-interface/workflows/Lint/badge.svg)](https://github.com/Uniswap/uniswap-interface/actions?query=workflow%3ALint)
[![Tests](https://github.com/Uniswap/uniswap-interface/workflows/Tests/badge.svg)](https://github.com/Uniswap/uniswap-interface/actions?query=workflow%3ATests)
[![Styled With Prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg)](https://prettier.io/)

===================

Morpheus Labs forked this the source code from UniSwap as a reference web application for proviuder Decentralized Swap functions like UniSwap. Users can explore, modify and test the web application on Morpheus Labs SEED platform.

Since this is a GNU License, for SEED platform users or any users who need to fork or clone the UniSwap Web App need to explicitly fork from this repo.

===================

An open source interface for Uniswap -- a protocol for decentralized exchange of Ethereum tokens.

- Website: [uniswap.org](https://uniswap.org/)
- Interface: [app.uniswap.org](https://app.uniswap.org)
- Docs: [uniswap.org/docs/](https://uniswap.org/docs/)
- Twitter: [@UniswapProtocol](https://twitter.com/UniswapProtocol)
- Reddit: [/r/Uniswap](https://www.reddit.com/r/Uniswap/)
- Email: [contact@uniswap.org](mailto:contact@uniswap.org)
- Discord: [Uniswap](https://discord.gg/Y7TF6QA)
- Whitepaper: [Link](https://hackmd.io/C-DvwDSfSxuh-Gd4WKE_ig)

## Accessing the Uniswap Interface

To access the Uniswap Interface, use an IPFS gateway link from the
[latest release](https://github.com/Uniswap/uniswap-interface/releases/latest), 
or visit [app.uniswap.org](https://app.uniswap.org).

## Listing a token

Please see the
[@uniswap/default-token-list](https://github.com/uniswap/default-token-list) 
repository.

## Development

### Install Dependencies

```bash
yarn
```

### Run

```bash
yarn start
```

The info below is to help understand the dependencies.

### Configuring the environment (optional)

To have the interface default to a different network when a wallet is not connected:

1. Make a copy of `.env` named `.env.local`
2. Change `REACT_APP_NETWORK_ID` to `"{YOUR_NETWORK_ID}"`
3. Change `REACT_APP_NETWORK_URL` to e.g. `"https://{YOUR_NETWORK_ID}.infura.io/v3/{YOUR_INFURA_KEY}"` 

Note that the interface only works on testnets where both 
[Uniswap V2](https://uniswap.org/docs/v2/smart-contracts/factory/) and 
[multicall](https://github.com/makerdao/multicall) are deployed.
The interface will not work on other networks.

## Contributions

**Please open all pull requests against the `master` branch.** 
CI checks will run against all PRs.

## Accessing Uniswap Interface V1

The Uniswap Interface supports swapping against, and migrating or removing liquidity from Uniswap V1. However,
if you would like to use Uniswap V1, the Uniswap V1 interface for mainnet and testnets is accessible via IPFS gateways 
linked from the [v1.0.0 release](https://github.com/Uniswap/uniswap-interface/releases/tag/v1.0.0).


The dependencies can be seen from its file "package.json" as belows.

1. Smart contract

**@uniswap/governance**

https://github.com/Uniswap/governance
Governance contracts for the Uniswap protocol

**@uniswap/liquidity-staker**

https://github.com/Uniswap/liquidity-staker
Initial UNI liquidity staking contracts

**@uniswap/merkle-distributor**

https://github.com/Uniswap/merkle-distributor
A smart contract that distributes a balance of tokens according to a merkle root

**@uniswap/v2-core**

https://github.com/Uniswap/uniswap-v2-core
Core smart contracts of Uniswap V2

**@uniswap/v2-periphery**

https://github.com/Uniswap/uniswap-v2-periphery
Peripheral smart contracts for interacting with Uniswap V2

**Notice**

The deployed contract addresses can be found in this file:
https://github.com/Uniswap/uniswap-interface/blob/master/src/constants/index.ts

2. SDK 

**@uniswap/sdk**

https://github.com/Uniswap/uniswap-sdk
An SDK for building applications on top of Uniswap.

**@uniswap/token-lists**

https://github.com/Uniswap/token-lists
The Token Lists specification

**Notice**

There is no backend component.

