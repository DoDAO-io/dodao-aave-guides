## Header
This is the course header. This will be added on top of every page. Go to [DoDAO.io](https://www.dodao.io) to know more.

---

## AAVE NPM Packages


## @aave/core-v3, @aave/core-v2



## [@aave/coreV3](https://www.npmjs.com/package/@aave/core-v3)

This package contains the smart contracts source code and markets configuration (The underlying logic, and terms specified for the market to work) related to Aave Protocol V3. 
It uses Docker Compose and Hardhat as development environment for compilation, testing and deployment tasks.

You can install @aave/aave-v3-core as an npm package to your hardhat or truffle workspace to get access to contracts and 
interfaces provided by Aave V3

You can install `@aave/core-v3` as an NPM package in your Hardhat or Truffle project to import the contracts and interfaces:

`npm install @aave/core-v3`

Import at Solidity files:

```solidity
  import {IPool} from "@aave/core-v3/contracts/interfaces/IPool.sol";

  contract Misc {

    function supply(address pool, address token, address user, uint256 amount) public {
      IPool(pool).supply(token, amount, user, 0);
      {...}
    }
  }
```

The JSON artifacts with the ABI and Bytecode are also included into the bundled NPM package at `artifacts/` directory.

Import JSON file via Node JS `require`:

```
  const PoolV3Artifact = require('@aave/core-v3/artifacts/contracts/protocol/pool/Pool.sol/Pool.json');

  // Log the ABI into console
  console.log(PoolV3Artifact.abi)
```

## [@aave/protocol-v2](https://www.npmjs.com/package/@aave/protocol-v2)
Package contains smart contracts related to v2.

Just like @aave/core-v3, you can  install @aave/protocol-v2 as an NPM package by running `npm install @aave/protocol-v2`

You can import Solidity and ABI files, just like the V3 files shown above.


    


---
## Evaluation





##### The smart contract source code and market configurations for V3 are contained within which npm package?  

- [ ]  @aave/contract-helpers
- [ ]  @aave/protocol-js
- [ ]  @aave/protocol-v2
- [x]  @aave/coreV3





##### Aave V3 uses which of these tools to setup the development environment?  

- [ ]  Truffle
- [x]  Hardhat
- [x]  Docker Compose
- [ ]  None of these

    


---
## @aave/protocol-js


## [@aave/protocol-js](https://www.npmjs.com/package/@aave/protocol-js)

Contains smart-contract interfaces and Javascript libraries that allows user to interact with and develop applications using the Aave protocol.
 the user with libraries which provide methods to
 Using this library, the user can use many of the basic functionality/features of the Aave protocol.

#### Data Formatting methods
`formatUserSummaryData`:
Returns formatted summary of AAVE user portfolio including: array of holdings, total liquidity, total collateral, 
total borrows, liquidation threshold, health factor, and available borrowing power

`formatReserves`:
Returns formatted summary of each AAVE reserve asset.
 
 #### LendingPool 
It encloses various transaction methods and the underlying logic and smartcontract for **Lending pool V2**, of which we have talked about in detail. For a short summary,
Lending pool is just a smart contract which acts as a reserve (pool) of assets, lent by liquidity providers for the protocol to use
for loaning. 

It contains the following methods,
`deposit`:
When this function is called, it takes in the address of the depositor(user), the address of the reserve to deposit to(reserve),
the amount to be deposited (amount) as parameters.

`borrow`:
The user must set the ethereum address of the reserve he wishes to borrow against, the amount and the type of interestRateMode rate he wishes to borrow on. 
Note that, interestRateMode takes in values from the enum InterestRate, which contains 'none', 'stable', and 'variable' as values.

`withdraw`:
Invoked when the user needs to withdraw assets. onBehalfOf address can also be passed in as a parameter,
allows the withdraw action to be done onbehalf of another address. By default it points to user address.

there are other functions whose use cases are more particular,

`swapBorrowRateMode`:
Shifts the type of interest rate on the borrow position.

`setUsageAsCollateral`:
This is a function which allows the depositor to accept or deny a specific asset as collateral.
A boolean value of useAsCollateral is used to specify whether or not assets from this ethererum 
reserve can be used as collateral.

`liquidateCall`:
This function enables user to liquidate an undercollateralized position.
Takes in the address of the liquidator, the address of the borrower, ethereum address of the principle asset and the collateral asset,
The amount that the liquidator wants to liquidates as paramaters.

`swapCollateral`:
Allows user to change the collateral asset to another assets.

`repayWithCollateral`:
Allows the borrower to repay the loan with the collateral.
 
 #### Governance 
Contains smartcontracts and methods which will implement Aave governance in the Aave protocol. 
Methods that can be called,
`create` - creates a proposal, that needs to be validated by proposal validator.

`cancel` - cancels a proposal. when called by guardian, has relaxed conditions. When called by a regular user,
         executes given that the conditions placed on the executor are fulfilled.

`queue` - Queue the proposal, given that it is succeeded.

`execute` - Execute the proposal, given it is queued.

`submitVote` - This function allows the caller of the function to caste a vote for/ against the proposal that is executed.

`delegate` - This function allows the user to delegate his voting power to a chosen address.

#### Staking
Aave staking is covered in the coming steps.
 


    


---
## Evaluation





##### The functions that must mandatorily be successfully called on a proposal before it can be executed are?  

- [x]  create
- [x]  queue
- [x]  submitVote
- [ ]  delegate





##### `setUsageAsCollateral` method allows the user to?  

- [ ]  Use the collateral produced by borrower
- [ ]  Configure the amount of collateral to be produced by borrower
- [x]  Determine what assets are acceptable as collateral for the deposited collateral
- [ ]  None of these





##### onBehalfOf parameter is by default set to user, who is user?  

- [x]  msg.sender
- [ ]  Address of the user who deposits/ borrows/ etc.,.
- [ ]  Could be both A and B
- [ ]  Neither A nor B





##### Methods that concern with collaterals, allow the user to do which of the following?  

- [x]  Swap the collateral asset for another asset
- [x]  Use the collateral to repay loan
- [ ]  Withdraw all of the collateral on command
- [x]  Determine which assets can qualify for collateral

    


---
## @aave/contract-helpers, @aave/math-utils



## [@aave/contract-helpers](https://www.npmjs.com/package/@aave/contract-helpers):

To install contract-helpers with npm,

_npm install @aave/contract-helpers_ 

with yarn,

_yarn add @aave/contract-helpers_ 

The @aave/contract-helpers package offers a set of services which allow querying aggregated on-chain data via rpc.
It contains methods for generating transacations based on method and parameter inputs. 
Basically, it is used to read and write data on the protocol contracts. Could be thought of like something that facilitates the querying and writing of 
data from and onto the original aave protocol. It is part of a larger package, aave-utilities. Aave Utilities is a JavaScript SDK for interacting with V2 and V3 of the Aave Protocol.

## [@aave/math-utils](https://www.npmjs.com/package/@aave/math-utils):

To install math-utils with npm,

_npm install @aave/math-utils_

with yarn,

_yarn add @aave/math-utils_

The @aave/math-utils data formatting methods act as a layer on top of the chain data. Meaning, the methods provide the user with an interface to be able to
interact with, and in turn comprehend the chain data, which otherwise might not be "human readable".
The use-cases range from "human readable formatting" to "approximating accrual over time."


    


---
## Evaluation





##### which package offers a set of methods which allow querying aggregated on-chain data?
  

- [ ]  @aave/math-utils
- [ ]  @aave/contract-helpers
- [x]  @aave/coreV3
- [ ]  All of these





##### contract helpers package helps performs which of these functions?  

- [x]  Writing data on the protocol contracts
- [x]  Querying data from the protocol contracts
- [ ]  Altering the Aave protocol
- [ ]  Providing the user with data formatted to be used in the frontend





##### the @aave/contract-helpers and @aave/math-utils deal with  

- [x]  Data formatting methods
- [x]  Data querying and writing
- [ ]  Voting on proposals
- [ ]  Formatting of proposals

    


---
## @aave/periphery-v3



## [@aave/periphery-v3](https://www.npmjs.com/package/@aave/periphery-v3): 
This repository contains smart-contracts, which allow you to incentivize assets with multiple rewards in Aave V3 markets. 
It also contains UI helpers and other external smart contracts utilities related to the Aave Protocol V3.
It contains rewards controller and rewards distrubutor contracts, which help to standardize and incentivize the liquidity of deposits and borrows
in various Aave markets. The incentives now include multiple tokens instead of only one, unlike previous implementations of the same concept.

#### Rewards Distrubutor
The RewardsDistributor abstract contract contains all the storage and logic functions for proper accounting of the rewards supported in the protocol.
The contract supports multiple incentivized assets and multiple rewards with different emissions and distribution end per reward. Each reward must be an ERC20 compatible contract.

The rewards distrubutor contains methods with which you can query various data that can be used for proper accounting of the incentive system 
in the protocol.
 
 #### Rewards controller
The RewardsController contract is responsible of configuring the different rewards and the claim process. It inherits RewardsDistrubutor to handle the
distrubution of incentives.(Note: The contract that inherits RewardsDistributor is in charge to provide the userBalance and the totalSupply of each incentivized asset to the RewardsDistributor) 
The user does not have to stake or hold/ keep their assets locked in a smart contract. As long as the user has
tokens in their possession, the tokens will accrue the rewards.

The rewards can be claimed with fine-grain control with the variety of methods offered by RewardsController.

#### Transfer Strategies
They are smart contracts that contain the logic for transaction of assets, they are of two types.
The PullRewardsStrategy supports common ERC20 incentives pulled from an external vault. This strategy contract allows to integrate any ERC20 token that want to 
incentivize deposits or borrows at Aave markets. You must provide the "vault" address where to accumulate rewards at the moment of claim.

(Note that, In order for the PullRewardsStrategy to be able to send money on behalf of the vault, the PullRewardsStrategy contract must have  ERC20 approval
from the vault.)

The RewardsController performs external calls to the transfer strategy contracts when the user calls claimRewards functions from the Rewards Distrubutor contracts. 
The transfer strategy contract then uses custom logic to transfer the assets from the source to the destination.
The external function, performTransfer(address to, address reward, uint256 amount) is then called by the rewards distrubutor to transfer the
rewards to the user.  


    


---
## Evaluation





##### Periphery-v3 consists of which of these set(s) of smartcontracts?  

- [x]  RewardsDistributor
- [x]  RewardsController
- [x]  TransferStrategy
- [ ]  LendingPool





##### RewardsController inherits RewardsDistributor, which of these is/are significance of this inheritance?  

- [x]  RewardsController is in charge of providing the RewardsDistributor, the userBalance of each incentivized asset
- [ ]  RewardsDistrubutor provides the RewardsController with important getter and setter methods
- [x]  RewardsController provides RewardsDistrubutor with total supply of each incentivized asset.
- [ ]  Both A and B





##### Which of these actions can be performed by the RewardsController smart contract?  

- [ ]  Approve (whitelist) an address to be able to claim rewards on another address's behalf
- [ ]  Set the contract address that will determines the logic for the transfer strategy
- [ ]  Set an Aave Oracle contract to enforce rewards with a source of value
- [x]  All of these

    


---
## @aave/aave-stake-v2


## [@aave/aave-stake-v2](https://github.com/aave/aave-stake-v2)
This package contains a series of smart-contracts which are related to the staking of aave tokens and the incentivization system based on them.
The package contains 3 main smart-contracts,

#### **AaveDistrubutionManager:**
This smart contract contains the logic for the accounting, i.e., the calculation logic for the rewarding of staking tokens in AAVE.
The smartcontracts like AaveIncentivesController inherit this method, any contract that interacts with the user/ protocol in this package will inherit
the AaveDistrubutionManager. 


**StakedAave:**
Contract to stake AAVE token, to be connected with a slashing mechanism in order to secure the Aave protocol called Aave SM (Security Module). 
The users can stake their assets in these contracts and receive stkAAVE tokens in return. These tokens accrue the interests/ rewards accumulated by the 
user over a given time period until which this token will be incentivized. Once the rewards are accrued, they can be redeemed at any given moment.
But, withdrawal of staked AAVE tokens cannot be done instantly. There is a cooldown period after activation, only after the cooldown period ends can the user withdraw their staked tokens.

**AaveIncentivesController:**
Contract in charge of the incentives for activity on the Aave protocol, inheriting from the AaveDistributionManager. 
Each time an event involving any incentive for an user happens on the Aave protocol (i.e., a deposit or a withdrawal of staked tokens, redemption of rewards etc.,.), 
this contract is called to manage the update of the incentives state. In return, it provides the AaveDistributionManager with userdata and reserve data concerning the
given asset, to apply logic and come up with new terms for rewarding the user for staking the asset.


    


---
## Evaluation





##### Define a shortfall event
  

- [ ]  A deficit of users in the Aave ecosystem
- [x]  A decifit of assets in the money markets of Aave ecosystem
- [ ]  both A and B





##### Why is a cooldown period necessary on withdrawal of staked Aave tokens?  

- [x]  To avoid mass fund withdrawals during shortfall events
- [x]  To ensure that there is liquidity of Aave tokens in the ecosystem
- [ ]  To validate whether a withdrawl is done by the correct user
- [ ]  To avoid traffic on the blockchain





##### What kind of data does the AaveIncentivesController provide the AaveDistributionManager?  

- [ ]  User data concering particular asset
- [ ]  Reserve data concerning particular asset
- [x]  Both A and B
- [ ]  User and reserve data about all the assets in the ecosystem.

    


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

- Aave v3 contracts with The3D | Solidity Fridays https://www.youtube.com/watch?v=l5RKksbi8e8
    
