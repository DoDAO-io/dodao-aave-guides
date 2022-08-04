## Header
This is the course header. This will be added on top of every page. Go to [DoDAO.io](https://www.dodao.io) to know more.

## Best AAVE Resources
V3 Videos
- https://www.youtube.com/watch?v=LzaS8IiqnPY
- https://www.youtube.com/watch?v=l5RKksbi8e8
- https://www.youtube.com/watch?v=JhuD6LnxMLE

V2 
- https://www.youtube.com/watch?v=vgOnZkjifAs
- https://www.youtube.com/watch?v=AMAMvKc-O2s
- https://www.youtube.com/watch?v=EzY9zFslRp0
- https://www.youtube.com/watch?v=9k-D57Mi-Qk
- Aave: Developer 101 - https://www.youtube.com/watch?v=WPG7T1dFLxQ

Cetora(Many developer videos) - https://www.youtube.com/channel/UC4DzjIwy_5afMxSI4mOpLHw/videos

---

## Intro to AAVE V3


## Overview

Centralization and illiquidity are two prevalent problems that DeFi, the blockchain, and other crypto-based 
projects devote to finding solutions to because illiquidity can affect users’ ability to get fair rates for 
their digital assets.

The demand for DeFi is growing, and so is interest from the traditional finance space and its institutions. In 
recent times, some hedge funds, asset managers, fintech, and family offices have shown interest in leveraging a 
version of Aave to handle internal requirements.

This is because the Aave protocol is one of the unique solutions to the drawbacks of centralization and 
illiquidity. The protocol is non-custodial liquidity and decentralized protocol. With Aave, users can 
participate as liquidators, suppliers, or borrowers.

Since the protocol’s launch in 2020, it has been at the forefront of championing DeFi innovations. Two factors 
have placed Aave V3 as one of the biggest DeFi protocols: An IPFS-deployed open-source frontend and AAVE’s 
unique governance controls.

The Aave protocol has already reached peak liquidity of $30B. On it, borrowers can borrow funds in an 
overcollateralized manner and partake in one-block borrow transactions or flash loans. These flash loans do not 
need over-collateralization.

Conversely, suppliers provide much-needed liquidity to markets and earn interest from cryptocurrency assets. 
Meanwhile, Aave V3 is a product of robust community feedback, ecosystem growth, and continuous iteration.

The Aave V3 of the protocol enhances the protocol’s core concept of stable rate borrowing, aTokens, instant 
liquidity, etc., with some new features and improvements like enhanced decentralization and security.

Capital efficiency is one of the significant utilities of the V3 as it allows users to optimize their digital 
assets supplied to Aave in terms of borrowing power and yield generation. Efficiency mode, portals, decentralization, 
and more, are some of the features we discuss that the Aave protocol uses to achieve capital efficiency.


    


---
## Evaluation

 



##### What major pair of solutions does Aave bring to the problems of centralization and illiquidity in DeFi?  

- [ ]  Inconvenient user interface
- [x]  Non-custodial liquidity and decentralized protocol services
- [ ]  Lack of crypto pairs
- [ ]  Expensive withdrawal fees

    


---
## AAVE V3 - New Features

## AAVE V3 High-Efficiency Mode
The Aave V3’s efficiency mode helps maximize and boost capital efficiency when borrowed and collateral assets are 
correlated in price. It is especially helpful when collateral and borrowed assets are the derivatives of one underlying 
asset, like stablecoins pegged to the dollar.

Meanwhile, since stablecoins are typically pegged to a specific asset, the chance of suddenly losing the peg is 
slim and near impossible. Cryptocurrencies like ETH and their derivatives like alETH, stETH, sETH, etc., have 
similar characteristics and behavior as their underlying asset.

Unique cases like this have the possibility of permitting high collateralization power. However, in the original 
Aave protocol design, borrowed assets and collateral value are normalized to a base currency such as USD or ETH.

This makes it impossible to know, on-chain, the specific collateral that is backing a corresponding borrowed asset,
making it difficult to enhance collateral efficiency. But all of these difficulties change with the help of Efficiency 
mode or E-Mode.

Efficiency Mode offers an asset classification that categorizes all assets that the Aave protocol lists. In effect, 
all assets in the same category will typically be highly correlative or mutually related in price.

This system can’t enforce the correct categorization on-chain because it also requires maintenance by whatever 
entity manages the protocol—the Aave governance. However, it is no cause for worry because this Efficiency Mode 
brings more freedom and choice.

Users can freely choose to borrow a specific category and employ high collateralization power, even using collaterals 
from the same category. In all, Efficiency Mode allows the introduction of a specific price oracle for a particular 
category.

## AAVE V3 Decentralization
Aave has introduced Asset Listing Admins with the V3. It is a unique role that the Aave governance grants to allow 
different asset listing strategies in addition to on-chain vote from Aave V2.

Asset Listing Admins will enhance decentralization and allow builders to make custom asset listing strategies. 
These strategies will surely bring true permissionless asset listing to the protocol.

As a feature in Aave, decentralization ensures protocol management is fully decentralized, and Aave token holders 
control it via Aave governance. Meanwhile, the Aave governance is the gatekeeper of some aspects of the protocol 
configuration, such as in listing new assets.


    


---
## Evaluation

 



##### High Efficiency Model is applicable to what type of assets?  

- [ ]  Assets with high volatility
- [ ]  Assets who value remain the same all the time
- [ ]  Only to stable coins
- [x]  Assets with the same/similar underline asset like alETH, stETH, sETH, etc. or Stable coins





##### Which of the followin is true regarding Asset Listing in AAVE v3  

- [ ]  Asset Listing Admins will enhance decentralization and allow builders to make custom asset listing strategies
- [x]  Asset Listing will only be allowed by core AAVE members
- [ ]  Anyone will be allowed to list an Asset on AAVE.
- [ ]  No new Assets will be listed in AAVE v3

    


---
## AAVE V3 - New Features

## AAVE V3 Isolation Mode
In Aave V2, when a new   asset is listed, the whole liquidity pool is exposed to it, meaning that users using the 
new collateral asset might be able to borrow the whole liquidity available. This greatly limits the capability 
to add new assets to the Aave Protocol, as every new asset increases the liquidity and solvency risk. Isolation 
mode solves for this

Aave V3’s Isolation Mode allows the protocol to list assets as “isolated easily.” Assets listed have a specific 
debt limit, and borrowers who decide to use an isolated asset as collateral can do so.  

However, if they need to, Aave V3 protocol users of isolated assets can supply other assets for yield generation. 
The flag “Borrowable In Isolation” indicates assets that users can borrow in isolation mode.

## AAVE V3 Portal
Portal indicates a series of core features that permit the seamless flow of supplied assets between Aave instances 
on various networks. Meanwhile, the Aave protocol exploits the rare designs of the aToken in burning aTokens on 
source networks.

It also allows instant minting on destination networks. The Aave protocol requires three extra features to support 
Portal in V3, namely:
* **Mint Unbacked Tokens**: Mint Unbacked Tokens allows addresses with Bridge role permission to mint unbacked 
  aTokens to onBehalfOf address.
* **Back Unbacked Tokens**: Back Unbacked Tokens permits contracts with Bridge role permission to back the unbacked 
    aTokens with the amount of the underlying asset and pay the necessary fee.
* **Whitelist Bridges**: Whitelist bridges permit the Bridge Role Admin to either remove or add the address for 
    the Bridge Role.


    


---
## Evaluation

 



##### What are the new features that are added to AAVE protocol to enable Portals  

- [ ]  Additional features that enable portals are "Web Service calls" and "Webhooks"
- [x]  Additional features that enable portals are "Mint Unbacked Tokens", "Back Unbacked Tokens" and "Whitelist Bridges"
- [ ]  Additional features that enable portals are "High Efficiency" and "Further Decentralization"

    


---
## AAVE V3 - Risk Management

Aave V3 offers a significantly enhanced set of risk parameters and improved features to help secure the protocol 
from potential insolvency. Here are some ways Aave achieves this:

### Supply and Borrow Caps
The Aave V3 relies on supply and borrow limits while allowing the protocol’s governance to configure Borrow and 
Supply caps. The Borrow Caps allow the adequate modulation of the amount of an asset borrowed, reducing the risk 
of insolvency.

On the other hand, Supply Caps limits the number of asset users can supply to the protocol. It helps reduce the 
exposure to a specific asset while reducing attacks such as price oracle manipulation or infinite minting.  

### Granular Borrowing Power Control  
The coming of Aave V3 brings granular borrowing power control that will allow the protocol to lower the borrowing 
power of assets to 0%. In addition, such control won’t have an impact on existing borrowers.

### Risk Admins
Aave V3 also introduces to users the ability for the Aave Governance to particular entities the permission to update 
risk parameters, and they can do this without requiring a governance vote.

The relevant entities could be automated agents like Gauntlet, RiskDAO, or just DAOs that can improve this feature 
to react mechanically in unforeseen circumstances. Meanwhile, Aave governance is capable of adding new Risk Admins 
or revoking access to existing ones.

### Price Oracle Sentinel
This feature carries a grace period for liquidations and disables borrowing in the face of specific scenarios. By 
design, it is built for L2s to handle potential downtime that may disrupt activities of the sequencer.

### Variable Liquidation Close Factor
Finally, in Aave V3, there is an improved liquidation mechanism from allowing liquidation of half of the position 
at a specific time to allowing the position to become fully liquidated when it nears insolvency.


    


---
## Evaluation

 



##### Aave V3 allows the protocol’s governance to configure what type of cap/s?  

- [ ]  Only Borrow
- [ ]  Only Supply
- [ ]  There are no Supply or Borrow Caps
- [x]  Both Supply and Borrow caps

    


---
## AAVE Vision and Goals

## AAVE Vision 
Aave believes in creating a protocol that can convert centralized financial services over to decentralized 
equivalents. The protocol also has the vision of creating a transparent, permissionless, and open-source financial 
service environment that encourages everyone to interact. Aave further seeks to remain compatible with other 
decentralized protocols via aTokens.

## AAVE Goals
The aim and goals of Aave are to build an algorithmic loan market that allows the following:

* Create a platform that can offer loans with different collaterals, operating policies, and collateralization 
  options. This is so that the protocol can adjust to the needs of different markets and its many users.
* Invest funds in pools to generate liquidity. Doing this should allow the users to offer loans to other users 
  who need them while also earning interest as liquidity providers.


    


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
    
