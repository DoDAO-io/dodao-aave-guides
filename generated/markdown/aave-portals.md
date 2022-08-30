## Header
This is the course header. This will be added on top of every page. Go to [DoDAO.io](https://www.dodao.io) to know more.

---

## AAVE Portals


## Overview

### Layer 2 Blockchains 
In 2020, we had seen a lot of people using Ethereum, and transaction requests increased. However, Ethereum 
can only handle 30 transactions per second. This limitation caused gas prices to hike and transactions to become expensive.

On Ethereum mainnet, transactions can be slow and difficult, and the proof-of-work model can use a lot of energy. So we need an alternative 
that can improve these issues without compromising decentralization and security.

Layer 2 chains offer an alternative to the high transaction costs and slow speeds of Ethereum blockchain. The main reason Layer 2 blockchains 
exist is to increase the scalability of the blockchain. As the number of users grows exponentially, we need to find a way to scale up the network without 
sacrificing decentralization and security.

### Reasons they exist include 
1. Busy network, which makes Ethereum-based transactions expensive. 
2. Low transaction throughput (the Ethereum network can handle 30 transactions per second).  

### Disadvantages of multiple blockchains
* It leads to confusion to choose among them. 
* The assets will be split into different chains, so it will be difficult to integrate them as we are required to 
  pay a fee for asset transfer from chain to chain.
* Most Defi protocols and marketplaces are Ethereum based, so we need to move our assets from one chain to another.


    


---
## Evaluation





##### What are the reasons for the existence of Layer2?  

- [ ]  To compete with the Ethereum
- [x]  Low transaction fee
- [x]  High transaction throughput
- [ ]  None of these





##### What are disadvantages with multiple blockchain?  

- [x]  The assets are segregated
- [ ]  It leads to competetion between the networks
- [ ]  Makes the transfer faster
- [ ]  None of these

    


---
## Tranferring assets using Blockchain bridges

## Why do we need to transfer our assets from one chain to another?
* **Transaction fees** - Layer2 networks boast transaction fees that are significantly lower than those on the Ethereum 
  main network. As a result, we often transfer our assets over to Layer2 in order to take advantage of the low fees.
* **Transaction speed** - Low transaction speed is a big pain point for Ethereum network as it can process only 30 
 transactions per second. This is a very low transaction throughput and causes a lot of inconvenience for users. 
 So, we switch to other networks for fast transactions.
* **Higher return on investment** -  transferring assets to blockchains with high-interest rates or liquidity for trading.
* **Capital utility/efficiency** - Able to use all assets from all blockchains in one transaction.

What are Blockchain Bridges?
Bridges in crypto act as a connection between two different blockchains. This connection is important because, 
without a bridge, blockchains would be isolated from each other. This is because each network has its own set of 
rules, governance mechanisms, and protocols. Ethereum is currently based on a Proof-of-Work mechanism, while 
other blockchains have different mechanisms, like Proof-of-Stake, Proof-of-Space, etc.

However, with a bridge between two blockchains it becomes possible to transfer crypto-assets and arbitrary data between them. 
Thus, bridges are essential for interoperability in the crypto ecosystem and are necessary to make different blockchain networks compatible.

## How bridges work?
We choose a bridging protocol to transfer our assets. Then, the bridge contract in the source chain will lock our 
assets so that the supply remains constant.  

The bridge contract will then mint an equivalent amount of wrapped tokens of the assets to the bridge contract in 
the destination network. The contract in the destination network will verify and send the wrapped assets to our account.

These wrapped assets can then be used for Defi protocols which have the same value as the original coin in the 
native network. So we can exchange the wrapped assets for other tokens or coins, or else we can get back our coin, 
for which we need to reverse the process in which the wrapped assets are pegged for the original coin in the 
equivalent amount.


    


---
## Evaluation





##### Why we need to tranfer our assets from chain to chain?  

- [ ]  More Valuable in other chains
- [x]  Transaction fee may be lower in other chains
- [x]  Opportunities in Liquidity pools of other chains
- [ ]  To secure our assets





##### What are Blockchain Bridges?  

- [ ]  It is a crypto bridge which connects bitcoin and Ethereum network only.
- [ ]  It is a network like Ethereum
- [x]  It is a crypto bridge which connects different networks
- [ ]  It is a token





##### What are Wrapped tokens?  

- [ ]  It is token like
- [x]  The wrapped coin is a representation of a cryptocurrency from another blockchain
- [ ]  It is an assets like NFT
- [ ]  None of these

    


---
## Disadvantages of bridges

Disadvantages of Bridges
* **Smart contract risks** - This issue can occur in both trusted and trustless bridges, as both rely on smart 
  contracts. If there is a bug in a smart contract, assets could be hacked - for example, Solana's warmhole bridge 
  was exploited in February 2022. Source: [link](https://rekt.news/wormhole-rekt/).

* **Systematic Financial risks** - The majority of bridges use wrapped assets to mint canonical versions of original 
  assets on the new chain. However, this exposes the bridge to systematic risks, as there is always the potential 
  for wrapped tokens to be exploited
* **Trust issues** - While other bridges use the third party as verifiers for the transfer of assets, this will 
  require users to put their trust in the assumption that validators will not engage in activities that would be 
  detrimental to users, such as rug pulling, censorship, or other suspicious activities.
* **Nascent stage** - The bridges are still in its infancy, and a lot of key questions have yet to be 
  answered. For example, it's still unclear how these bridges will perform in a variety of different market 
  conditions. The process of settling transaction on a bridge can also be quite time-consuming in some cases.


    


---
## Evaluation





##### What are the issues with Bridges?  

- [ ]  It is very complicated to use
- [x]  Trust issues will happen when the validators are third party
- [x]  there will be smartcontract risks
- [x]  It is in nascent stage and might take a lot of time for the transactions which gives awful user experience.





##### Which of the following is correct about bridges?  

- [ ]  Bridges have no issues and super efficient for transferring assets
- [ ]  Bridges help move assets from one chain to other
- [x]  It has smartcontract issues and trust issues
- [ ]  None of these

    


---
## AAVE Portals and how it simplifies the things

Portal's feature seamlessly allows assets to flow between Aave markets on different networks. Aave allows specific 
whitelist entities or specific bridges to burn atokens (atokens are nothing but AAVE’s token, which refers to a 
particular token as aDai refers to Dai ) in the source network and instantly minting them on the destination 
network. The underlying assets are then transferred to the destination network in a deferred manner(postponed manner) 
by passing it to the pool after it has been moved through the bridge. 

Portals are authorized for only approved bridges by Aave Governance. The assets are moved under smart contracts, 
making the transactions highly secure. Transactions with this system are quick and easy, so users will be able to 
save time. Many people will be attracted to the Aave portal because of its features, which will in turn increase the 
amount of capital in Aave markets. This also encourages other alt chains to use them as they have different kinds of 
features. 

Aave's new portal feature will help users overcome the difficulties of current bridging protocols, like 
liquidity fragmentation and non-optimal bridging experience. By reducing liquidity limitations of l2-l2 bridges, 
the portal will allow for a seamless experience for users.

Aave portals make it easy to transfer funds between different protocols by creating aTokens that are instantly 
minted on the destination network. Aave's unique pooling system is trustless and secure. The assets are transferred 
to the Aave pool on the destination chain after the burning and minting of aTokens.

Aave portals can also contribute significant growth to rollups (scaling solution for Ethereum), so the user 
experience of the network also increases. It acts as a gateway for some alt Evm L1 (alternate chains) which are 
heavily connected to centralized finance. However, Cefi's are slow to support a multiverse of chains. They are not 
supporting alternative networks, which complicates onboarding new users as it can be costly and difficult to reach 
alternatives. So having portals on these networks reduces the difficulties by providing security and fast transactions, 
making alt Evm L1 attractive and easier to access.


    


---
## Evaluation





##### What are the issues with the bridges does Aave portals solves?  

- [x]  It solves the time complexity as the assets are transferred instantly by using Aave portal feature
- [x]  It is very user firendly as user doesn't have to go through the process of transferring the assets to different bridges
- [ ]  It gives interest for transfering assets
- [ ]  It reduces the transaction fee for bridges





##### which of the following are correct about Portals?  

- [x]  Only specific approved bridges are allowed to mint unbacked aTokens and withraw assets from the destination network to the user's account.
- [x]  Users cannot directly access Aave Portals
- [ ]  It makes bridges difficult to transfer
- [ ]  Users gain interest on transferring assets

    


---
## How Portals work

In order to bridge assets from one chain to another, the user first submits a bridge transaction to a verified 
bridging protocol (such as Connext). As soon as the transaction is mined, the user has access to the funds on the 
destination chain. 

Behind the scenes, the bridging protocol mints unbacked aTokens on the destination chain to the intermediate 
contract, and in turn withdraws and transfers the underlying asset to the user immediately. The bridge contract on 
L2 then supplies the underlying asset and fee to the Aave pool to back the previously minted unbacked aTokens. 

Later, once the funds are available on L2, a bridge contract on L2 (for example, with BRIDGE permissions on Aave V3) 
can provide the underlying asset and fee to the Aave pool in order to back the previously minted unbacked aTokens.

Note: Only approved bridges use this portal feature, so there is no risk of withdrawing funds from Aave v3. Also, Aave 
portals are just a feature to transfer assets efficiently, but we need bridging protocols to transfer our assets; 
there are no other core protocols for directly using Aave portals from the user end. 

Let's say you want to transfer 50k Dai from Ethereum (L1) to Arbitrum (L2). You'd make a transaction request in Hop, 
and your assets would get deposited in Hop's liquidity pool. Then, Aave V3 would instantly withdraw the assets to 
your account in Arbitrum. On top of that, it would mint unbacked atokens according to the asset transfer. The 
transaction fee would depend on the bridging protocol you're using.

The "bridge" is used to store assets supplied by multiple users in a pool, and then to batch them together. The 
"hop" will use tokens to withdraw the assets from the pool, and then use its own bridging protocol to transfer the 
assets from Ethereum to Arbitrum. The bridge contract in Arbitrum will back the minted unbacked tokens, and reduce 
the fee for using Aave v3 portals. 

This is how portals enable seamless transactions between markets in different networks. Also, the bridges are 
approved, and assets are transferred under smart contracts Hence the transactions are secure.


    


---
## Evaluation





##### what is the fee for Bridges which are using Aave portals?  

- [ ]  20% of their transaction fee which they charge to user
- [x]  Fee is decided by Aave Governance
- [ ]  It depends on how long they are using that feature
- [ ]  No fees at all





##### Which of the following are not correct about working of portals?  

- [ ]  Aave leverage specific bridges to mint unbacked atokens and withraw assets from Aave market in the destination network
- [x]  The Portals directly transfer user's assets from one chain to another
- [x]  Portals just verifies the transaction by the bridging protocols.
- [ ]  The assets are transferred in a deferred manner with te help of smart-contracts

    


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

- Aave v3 contracts with The3D | Solidity Fridays https://www.youtube.com/watch?v=l5RKksbi8e8
    
