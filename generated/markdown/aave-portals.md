## Header
This is the course header. This will be added on top of every page. Go to [DoDAO.io](https://www.dodao.io) to know more.

---

## AAVE Portals


## Overview

## Layer 2 Blockhains and its disadvantages 
In 2020, we have seen gas prices hike, and transactions are expensive. Have you thought about why this has happened this all happened due to the 
increased users and a lot of transaction requests which the Ethereum main chain cannot handle as Ethereum was able to handle only 30 transactions per second.
This makes the transactions more difficult and time-consuming also, the proof-of-work model consumes a lot of energy for mining, so we need an upgrade for 
this issue without compromising decentralization and security.
So, we need alternate chains or enhanced mainchains so the intensity in the mainnet will decrease and the transactions will be more feasible. 
So we started to move on to scale the Ethereum network.
The main reason is to scale up the blockchain technology as the number of users grows exponentially we need to scale up the network 
without sacrificing decentralization and security. The solution is to create a layer 2 solution or create efficient chains so it can handle the scaling problems.

Reasons they exist include 
1. High fees for the transaction 
2. Busy network, which makes Ethereum-based transactions expensive. 
3. low transaction throughput (the Ethereum network can handle 30 transactions per second). 
4. The transactions are slow compared to centralized ones. 

Disadvantages of multiple blockchains
* It leads to confusion to choose among them. 
* The assets will be split into different chains, so it will be difficult to integrate them as we are required to pay a fee for asset transfer from chain to chain.
* some features in one chain will not be in another chain example, plasma chains do not compute, so they cannot run smart contracts. As we are scaling,
   we are required to sacrifice some other features in Ethereum to scale up the network, which leads to segregation and security loss.
* Most Defi protocols and marketplaces are Ethereum based, so we need to move our assets from one chain to another.


    


---
## Tranferring assets using Blockchain bridges

Why do we need to transfer our assets from one chain to another?
* Transaction fees- The transaction fees are very low in the polygon network compared to Ethereum main network. Hence, we transfer our assets from Ethereum to Polygon to enjoy low transaction fees. This is just one example even other networks have very low fees for transferring assets.
* Transaction speed- Transaction speed is very low in the Ethereum network as it can process only 30 transactions per second, which is a very low transaction throughput, so we switch to other networks for fast transactions.
* Liquidity Pools-  we will transfer assets to blockchains with high-interest rates or liquidity for trading.
* Capital utility/ efficiency-Able to use all assets from all blockchains in one transaction.

What are blockchain bridges?
bridges in crypto connect two different blockchains. This connection is important because, without a bridge, blockchains are siloed (isolated ) environments 
that cannot communicate with each other.This is because each network has its own set of rules, governance mechanisms, and different types of protocols 
Ethereum is currently based on a Proof-of-work mechanism, while other blockchains have different mechanisms, like Proof-of-stake, Proof-of space, etc.
However with a bridge between two blockchains it becomes possible to transfer crypto-assets and arbitrary data between them. 
Thus, bridges are essential for interoperability in the crypto ecosystem and are necessary to make different blockchain networks compatible.

How do they work?
First, we will choose a bridging protocol to transfer our assets. Then the bridge contract in the source chain will lock our assets so that 
the supply remains constant.Then issues or mints an equivalent amount of  Wrapped tokens of the assets to the bridge contract in the destination network 
so that the contract in the destination network verifies and sends the wrapped assets to our account.These wrapped assets then can be used for Defi protocols 
which have the same value as the original coin in the native network.So we can exchange the wrapped assets for other tokens or coins, or else we can get back our coin,
for which we need to reverse the process in which the wrapped assets are pegged for the original coin in the equivalent amount by using the bridge.


    


---
## Evaluation





##### Why we need to tranfer our assets from chain to chain?  

- [ ]  More oppurtunities
- [x]  Transaction fee may be lower in other chains
- [x]  Oppurturnities in Liquidity pools in other chains
- [ ]  To secure our assets

    


---
## Types of transfer and disadvantages of bridges

Bridging protocols transfer assets from one chain to other chains in three methods
1. **Lock and mint**: In this method, the assets are locked in the source blockchain and minted (creation of tokens) in the destination chain the locked assets 
                      can't be used after bridging. This is the method that we saw above.

2. **Burn and mint**: In this method, assets are burnt (destroyed) in the source blockchain and minted or created in the destination blockchain. 
                      Example [Hop](https://hop.exchange/), [across](https://across.to/).
                      In this method, instead of locking the original assets, it is completely destroyed this will happens in the case of token transfers as tokens don’t have a native blockchain.

3. **Atomic swaps** : In this method, assets are swapped from source chain to destination chain using smart contracts, which removes the trust issues and 
                     involvement of third-party. Example [connext](https://www.connext.network/).unlike locking or burning, the assets are swapped with the help of smart contracts.

Disadvantages of Bridges
* **Smart contract risks** - This issues can occur in both trusted and trustless bridges as both depend on smart contracts. If there is a bug in a smart contract,
                            there is a possibility of hacking assets, for example, Solana’s warm hole bridge. Source: [link](https://rekt.news/wormhole-rekt/).
* **Systematic Financial risks** - Most of the Bridges use wrapped assets to mint canonical versions of original assets in the new chain. This exposes the 
                                    bridge to systematic risks as there is the possibility of wrapped tokens getting exploited.
* **Trust issues** - Some bridges use the third party as verifiers for the transfer of the assets, that require users to rely on the assumption that validators 
                    will not collude to steal our funds. This will include being rug pulled, censorship, and other suspicious activities.
* **Nascent stage** - The bridges are in the nascent stages of development, so there are a lot of unsolved questions, like 
                    how bridges will perform in different market conditions.The transaction might take a lot of time in some cases.


    


---
## Evaluation





##### Which of the following bridging protocol using atomic swaps for transferring assets?  

- [ ]  Polygon's Pos bridge
- [x]  connext
- [ ]  hop protocol
- [ ]  across protocol





##### What are the issues with Bridges?  

- [ ]  It is very complicated to use
- [x]  Trust issues will happen when the validators are third party
- [x]  there will be smartcontract risks
- [x]  It is in nascent stage and might take a lot of time for the transactions which gives awful user experience.

    


---
## AAVE Portals

**AAVE Portals and how it simplifies the things** 
Portal's feature seamlessly allows assets to flow between Aave markets on different networks. Aave allows specific whitelist entities or specific bridges to 
burn atokens (atokens are nothing but AAVE’s token, which refers to a particular token as aDai refers to Dai ) in the source network and instantly minting 
them on the destination network. The underlying assets are then transferred to the destination network in a deferred manner(postponed manner) by passing it to 
the pool after it has been moved through the bridge. 

First of all, the transfers using portals are authorized for only approved bridges by Aave Governance, so the security is very tight. Also, the assets are 
moved under smart contracts. The transactions are instant, so the user experience will be nice and users time is also saved. By this, many people will be 
attracted and start to use Aave portals, so the capital in Aave markets also increases drastically; this also encourages other alt chains to use them as 
they have different kinds of features. So in simple words, it reduces all sorts of risks that we have seen in bridges not using Aave portals and the 
transactions are very fast or instant, which is a great negative for normal bridging protocols.

So let us see what Aave portals are doing and simplify the issues by bridging protocols so first of all, the transfer is an instant process as the 
atokens are minted instantly on the destination network, and the funds are transferred to the user instantly, so the bridging process is very fast. 
Aave portals are ready-made fast exit solutions it mitigates the transportation by bridges. Users will experience seamless transfer speed by portal feature.
The portal feature make it very secure as only approved bridges can use this feauture and all the transfers are done by smartcontracts so it is very secure.
Also no matter what the market conditions the transfer is instant and guaranteed.So there is no trust issues,instant transactions,very secure, 
Transactions doesn't affected by any external condition , also it increases the capital efficiency of Aave protocol.Thus it solves almost  all the 
issues faced with bridges.


    


---
## Evaluation





##### What are the issues with the bridges does Aave portals solves?  

- [ ]  It solves the time complexity as the assets are transferred instantly by using Aave portal feature
- [ ]  It is very secure and it connects variety of networks with Aave markets
- [ ]  It gives interest for transfer
- [ ]  It reduces the transaction fee for bridges

    


---
## How Portals work

So first, the user sends Bridge tx to the bridge protocol. The Aave portals leverage the bridge to mint unbacked atokens in the destination network and 
withdraw assets from the Aave liquidity pool in the destination network and send them to the user’s wallet. immediately from Aave v3. 

Now let us see how Portals makes transfers easily first, the approved bridges batch multiple users tx and then move assets from the source network to the 
destination network this makes them very efficient as the funds are transferred instantly to the users, and then transactions are bulked together and 
transferred to the destination in a deferred manner so it reduces a lot of time and congestion in the bridge network so people will be attracted to the bridges 
Which are using Aave portal feature as the whole process is very trustable and an efficient process.

Once the assets are transferred by the bridging protocol, then the Bridge contract in L2 moves them to Aave v3 in the destination to back the unbacked atokens, 
which were minted whenever users transfer funds. As this process is based on the smart contract, in this case the bridge contract supplies the assets to 
Aave protocol, so there is no risk involved with this transfer also, only approved bridges are able to use this feature, so security is perfect.There is a fee
deduction for bridges for using the Aave's portal feature which will be deducted automatically by the bridge contract.

**Note: Aave portals are the only feature to transfer assets using bridges there is no core protocol for transferring directly from the user end.**

In simple words, the user's assets are directly provided by Aave in the destination network. Then the bridges withdraw assets using the atokens means it burns 
them to withdraw from Aave. Then they batch multiple transaction assets and send them to the destination network. Then the bridge contract will exchange the 
assets for atokens with a fee. This is how bridges use Aave’s portal to transfer assets by using them, there is no other third party, no trust issues, 
instant transactions for users, very good user experience; this also increases the liquidity of the Aave protocol as, by this, a lot of users can seamlessly 
transfer funds without worrying. The fee which is provided to Aave will be decided by Aave governance.


    


---
## Evaluation





##### How to use or access Aave portals for a normal user?  

- [x]  We cannot directly ue it from user end but we can use a bridge which is a approved bridge by Aave governance ans also uses aave portal feauture
- [ ]  We can use it by any bridging protocol
- [ ]  We can use it by directly in Aave's website
- [ ]  We can use them by deploying smartcontracts like in flashloans





##### what is the fee for Bridges which are using Aave portals?  

- [ ]  20% of their transaction fee which they charge to user
- [x]  Fee is decided by Aave Governance
- [ ]  It depends on how long they are using that feature
- [ ]  No fees at all

    


---
## Your Info





| Label | Type | Required |
| ----------- | ----------- | ---- |
| Nick Name        | PublicShortInput   |  true    |




    


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
    
