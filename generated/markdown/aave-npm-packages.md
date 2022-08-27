## Header
This is the course header. This will be added on top of every page. Go to [DoDAO.io](https://www.dodao.io) to know more.

---

## AAVE NPM Packages


## @aave/core-v3, @aave/core-v2



## @aave/coreV3
This package contains the smart contracts source code and markets configuration related to Aave Protocol V3. 
It uses Docker Compose and Hardhat as development environment for compilation, testing and deployment tasks.

You can install @aave/aave-v3-core as an npm package to your hardhat or truffle workspace to get access to contracts and 
interfaces provided by Aave V3

The repository uses Docker Compose to manage sensitive keys and load the configuration. 
Before any action like test or deploy, you must run docker-compose up to start the contracts-env container, and then connect to the container console through docker-compose exec contracts-env bash.
You can run a full test suite using Docker Compose commands.

## @aave/coreV2
This is the previous version of Aave core V3. and so it has features similar to V3.
The repository uses Docker Compose to manage sensitive keys and load the configuration. 
Prior any action like test or deploy, you must run docker-compose up to start the contracts-env container, and then connect to the container console via docker-compose exec contracts-env bash.


    


---
## Evaluation





##### The smart contract source code and market configurations are contained within which repo?  

- [x]  Aave core V3
- [ ]  Math util
- [ ]  Lens protocol
- [ ]  None of these





##### Aave V3 uses which of these as development environment?  

- [ ]  Truffle
- [x]  Hardhat
- [x]  Docker Compose
- [ ]  None of these





##### Which of these packages enable stake of Aave related assets?  

- [x]  Aave-stake
- [ ]  Truffle commands
- [ ]  Aave Core v3
- [ ]  None of these

    


---
## @aave/aave-token


## @aave/aave-token:
The AAVE token is an ERC-20 compatible token that implements governance-inspired features. This will allow Aave to bootstrap the rewards program for safety and ecosystem growth. 

**Roles:**
The original AAVE token contract does not have any administrator roles set up. The contract will use the Openzeppelin implementation of the EIP-1967 Transparent Proxy pattern, which will have an administrator role. 
The proxy's administrator will be set when the contract is deployed to the Aave governance contracts.

The AAVE token implements the standard methods of the ERC-20 interface, with a balance snapshot feature to keep track of the balances of users at specific block heights. This is helpful for the Aave governance integration of AAVE.
AAVE also integrates the EIP 2612 permit function - which allows gasless transactions and one tx approval/transfer.

**LendToAaveMigrator:**
It is the smart contract for LEND token holders to execute the migration to the AAVE token, using part of the initial emission of AAVE for it.

The contract is covered by a proxy, whose owner will be the AAVE governance. 
Once the governance passes the corresponding proposal, the proxy will be connected to the implementation and LEND holders will be able to call the migrateFromLend() function, 
which, after LEND approval, will pull LEND from the holder wallet and transfer back an equivalent AAVE amount defined by the LEND_AAVE_RATIO constant.

Form the npm docs,
One tradeOff of migrateFromLend() is that, as the AAVE total supply will be lower than LEND, the LEND_AAVE_RATIO will be always > 1, causing a loss of precision for amounts of LEND that are not multiple of LEND_AAVE_RATIO. E.g. a person sending 1.000000000000000022 LEND, with a LEND_AAVE_RATIO == 100, will receive 0.01 AAVE, losing the value of the last 22 small units of LEND. 
Taking into account the current value of LEND and the future value of AAVE, a lack of precision for less than LEND_AAVE_RATIO small units represents a value several orders of magnitude smaller than 0.01$. 

**Redemption process:**
The Aave team will be responsible for the first step in bootstrapping AAVE emissions by deploying the AAVE token contract and the LendToAaveMigrator contract. Upon deployment, the ownership of the Proxy of the AAVE contract and the LendToAaveMigrator will be transferred to the Aave Governance. 
In order to start the LEND redemption process at that point, the Aave team will create an AIP (Aave Improvement Proposal) and submit it as a proposal to the Aave governance for approval.
The proposal will, once approved, activate the LEND/AAVE redemption process and the ecosystem incentives, which will mark the initial emission of AAVE on the market. The result of the migration procedure will see the supply of LEND being progressively locked within the new AAVE smart contract, while at the same time an equivalent amount of AAVE is being issued. The amount of AAVE equivalent to the LEND tokens burned in the initial phase of the AAVE protocol will remain locked in the LendToAaveMigrator contract. 
In other words, when you redeem your LEND tokens for AAVE, you're also locking up an equivalent amount of AAVE in order to ensure that there's no net increase in the total supply of AAVE.

The smartcontract can then be deployed to the testnet or the mainnet.


    


---
## Evaluation





##### Does the original Aave token have an administrator role set up?  

- [x]  No
- [ ]  Yes





##### Aave token is a?
  

- [ ]  ERC721
- [ ]  ERC42
- [x]  ERC20
- [ ]  none of these





##### Aave integrates EIP-2612 permit function.
  

- [x]  true

- [ ]  false


    


---
## @aave/contract-helpers, @aave/math-utils,  @aave/periphery-v3



## @aave/contract-helpers:
The @aave/contract-helpers package offers a set of services which allow querying aggregated on-chain data via rpc.
It contains methods for generating transacations based on method and parameter inputs. Basically, it is used to 
read and write data on the protocol contracts. Could be thought of like something that facilitates the querying and writing of 
data from and onto the original aave protocol.
It is part of a larger package, aave-utilities. Aave Utilities is a JavaScript SDK for interacting with V2 and V3 of the Aave Protocol

## @aave/math-utils:
The @aave/math-utils data formatting methods act as a layer on top of the chain data. 
The use-cases range from "human readable formatting" to "approximating accrual over time."
We know users interact with the aave protocol using smartcontracts, @aave/math-utils package is a collection of methods to take raw input data 
from these contracts, and format to use on a frontend interface such as Aave Ui or Aave info.

It formats two types of data, raw and indexed contract data, for front-end usage.
 * ethers.js: 
   ethers.js is considered raw contract data. ethers.js is a library for interacting with Ethereum and other EVM compatible blockchains.

 * subgraph:
   It is an indexed data type. Subgraphs work by indexing events that come from smart contracts. 
   This allows for data to be queried via a graphql endpoint. In other words, for each network where the protocol is deployed, there is a subgraph that corresponds to it.
 
 * Caching servers:
   The Aave UI uses decentralized hosting with IPFS, which means that it doesn't require any API keys to run. However, this also means that only public rpc endpoints can be used, which are quickly rate-limited. 
   To respond for this, Aave has published a caching server that performs contract queries on one server and then serves the data to all frontend users through a graphQL endpoint.
   
   (Note: GraphQL has been mentioned multiple times, for those who are unfamiliar - it is an open-source data query and manipulation language for APIs, and a runtime for fulfilling queries with existing data.)

## @aave/periphery-v3:
This repository contains the Rewards Controller contract, which allows you to incentivize assets with multiple rewards in Aave V3 markets. 
It also contains UI helpers and other external smart contracts utilities related to the Aave Protocol V3.


    


---
## Evaluation





##### which package offers a set of services which allow querying aggregated on-chain data?
  

- [ ]  UI kit
- [ ]  Math utils
- [x]  Contract helpers
- [ ]  All of these





##### Which of these acts as a layer on top of the existing chain-data?  

- [ ]  UI kit
- [x]  Math utils
- [ ]  Contract helpers
- [ ]  Aave tokens





##### mathutils formats which of these following data for use in frontend?  

- [x]  ethers.js
- [x]  indexed data
- [ ]  hardhat
- [ ]  None of these

    


---
## @aave/protocol-js, @aave/safety-module, @aave/protocol-v2



## @aave/protocol-js
AAVE is a decentralized non-custodial liquidity market protocol where users can participate as depositors or borrowers. 
The AAVE Protocol is a set of open source smart contracts which facilitate the lending and borrowing of user funds. These contracts, 
and all user transactions/balances are stored on a public ledger called a blockchain, making them accessible to anyone.

ethers js, something we discussed about earlier, is a peer dependancy (PeerDependency, it is not automatically installed. Instead, the code that includes the package must include it as its dependency.) for protocol-js.

The aave-js data formatting methods are a layer beyond graphql which wraps protocol data into more usable formats. Each method will require inputs from AAVE subgraph queries.
As you can see, we have already discussed about formatting packages (@aave/math-utils), these features are enclosed in this package. It has data formatting services which allow the querying of 
User data and reserve data.
It also encloses various transaction methods and the **Lending pool V2**, of which we have talked about in detail. For a short summary,
Lending pool is just a smart contract which acts as a reserve (pool) of assets, lent by liquidity providers for the protocol to use
for loaning. It contains methods like deposit, borrow, repay, withdraw, etc which can be called by users via smartcontracts.
It also encloses other vast concepts like aave governance.

## @aave/safety-module
The Aave Protocol is secured by a smart contract-based component called the Safety Module (SM). AAVE holders can lock tokens into the SM to incentivize them to act as a 
mitigation tool in case of a Shortfall Event within the Aave ecosystem. A Shortfall Event occurs when there is a deficit in one of the money markets that belong 
to the Aave ecosystem. The interpretation for the occurrence of a Shortfall Event is subject to the Protocol Governance vote.

The Safety Module is designed to work with existing AMM technologies. The module will have an 80% AAVE/20% ETH liquidity pool that uses Balancer. This is meant to provide benefits like market depth for the AAVE token and earnings from locking AAVE. 
The module will also cover BAL tokens and trading fees. Plus, it will reduce the impact of a Shortfall Event on the AAVE token.
In the event of a Shortfall, a portion of the locked AAVE is auctioned off to be sold in order to make up for the deficit. The SM has a built-in backstop mechanism to prevent too 
much AAVE from entering the open market, which would lower the value of AAVE. By locking AAVE into the SM, participants are accepting the possibility of a Shortfall Event occurring, 
in exchange for rewards in the form of Safety Incentives (SI).

AAVE holders can deposit their tokens into the Staking Mechanism to contribute to the safety of the protocol and receive incentives. In return, they will receive a tokenized position
that can be freely moved within the underlying network. The holder of the tokenized position can redeem their share from the SM at any time, triggering a cooldown period of 
one week (which can be further extended by the governance, mentioned in the protocol-js).

## @aave/protocol-v2
This repository contains the smart contracts source code and markets configuration for Aave Protocol V2. The repository uses Docker Compose and Hardhat as development enviroment for compilation, testing and deployment tasks.
This is bascially an all encompassing package which has all functions of the aave protocol as a whole. Helps the developer interact with the aave protocol from their development environment.


    


---
## Evaluation





##### @aave/protocol-js encloses which of these?
  

- [x]  aave governance
- [x]  aave lending pool
- [x]  data formatting and transaction methods
- [ ]  None of these





##### Safety Module is a?  

- [ ]  Smart contract based component
- [ ]  Component used to hold Aave tokens
- [x]  Both of these
- [ ]  None of these





##### How are the terms of a shortfall event decided?  

- [x]  Protocol governance votes
- [ ]  Popular opinion on twitter
- [ ]  Algorithms in the system
- [ ]  Both A and B





##### What is a peer dependancy?  

- [ ]  Dependancy that comes installed with the packages
- [x]  Dependancy that the package uses, but is not pre-installed.
- [ ]  Dependancy that is optional
- [ ]  None of these

    


---
## Footer
This is the course header. This will be added on top of every page. Go to [DoDAO.io](https://www.dodao.io) to know more.

## Best AAVE Resources
V3 Videos
- https://www.youtube.com/watch?v=l5RKksbi8e8
- https://www.youtube.com/watch?v=JhuD6LnxMLE

V2
- https://www.youtube.com/watch?v=vgOnZkjifAs
- https://www.youtube.com/watch?v=AMAMvKc-O2s
- https://www.youtube.com/watch?v=EzY9zFslRp0
- https://www.youtube.com/watch?v=9k-D57Mi-Qk
- Aave: Developer 101 - https://www.youtube.com/watch?v=WPG7T1dFLxQ

Cetora(Many developer videos) - https://www.youtube.com/channel/UC4DzjIwy_5afMxSI4mOpLHw/videos
- https://www.youtube.com/watch?v=LzaS8IiqnPY
    
