## Header
This is the course header. This will be added on top of every page. Go to [DoDAO.io](https://www.dodao.io) to know more.

---

## Decentralized Borrowing


## Important terms


Decentralized borrowing refers to the process of borrowing assets from a protocol run using smart contracts. In order to understand 
its workings and uses, we need to know a few of these important terms first.

- **Liquidation:** - The selling of collateral to cover the debt is called liquidation.

- **LTV (Loan to Value):** - Loan to value is the ratio used to decide how much loan can be borrowed against the 
  collateral produced. It is expressed in terms of percentages. (e.g., at LTV=75%, for every 1 ETH worth of collateral, 
  borrowers will be able to borrow 0.75 ETH worth of the corresponding currency). 

- **Liquidation Threshold:** - The liquidation threshold is the percentage at which a loan is deemed undercollateralized. 
  For example, a Liquidation threshold of 70% means that if the loan's value rises above 70% of the collateral, 
  the position is undercollateralized and could be liquidated.

- **Liquidation Penalty:** - The liquidation penalty is a fee rendered on the price of assets of the collateral when 
  liquidators purchase it as part of the liquidation of a loan that has passed the liquidation threshold.

- **Health Factor:** - It is a risk parameter that decides whether a borrow position is at risk of getting liquidated. 
  It is calculated by, `( H.F = ΣCollateral in ETH x Liquidation threshold / Total borrows )`


    


---
## Evaluation





##### Which two parameters decides the risk of a loan's liquidation?  

- [x]  Health Factor
- [ ]  Liquidation Penalty
- [ ]  Loan to Value
- [x]  Liquidation Threshold





##### The selling of collateral to cover for debt is?  

- [ ]  Health Factor
- [ ]  LTV
- [x]  Liquidation
- [ ]  None of these





##### LTV stands for  

- [x]  Loan to Value
- [ ]  Load to Vector
- [ ]  Loading the value
- [ ]  None of these





##### The percentage at which a loan is deemed undercollateralized:
  

- [ ]  LTV
- [ ]  Liquidation percentage
- [x]  Liquidation Threshold
- [ ]  None of these

    


---
## Borrowing in Traditional finance vs. DeFi

| ##Traditional Borrowing##  | ##DeFi Borrowing##  |
|---|---|
| Banks charge fees on top of premiums. | No fees clipped onto the borrower.|
| Borrowing from banks is very costly, high interest rates decided by central bodies.| The rates of interest are decided by basic supply and demand.  |
| Repayment time for borrowed amount is fixed. | Repayment time is indefinite, no problem as long as loan is not undercollateralized.|
| Slow and inefficient. No innovations lately.| Quickly developing and highly efficient.|
| Lengthy paperworks, legal agreements and steep qualifying criteria.| No qualifying criteria, all you need is a crypto wallet and money for gas fees.   |


    


---
## Evaluation





##### Which of these borrowing options is inefficient  

- [x]  Traditional loan
- [ ]  DeFi loan
- [ ]  Both of these
- [ ]  None of these





##### The limitations of Traditional finance are:
  

- [x]  Repayment time for borrowed amount is fixed
- [ ]  Quickly developing and highly efficient
- [x]  Lengthy paperworks, legal agreements and steep qualifying criteria
- [ ]  None of these





##### The advantages of DeFi are:
  

- [x]  Repayment time is indefinite, no problem as long as loan is not undercollateralized.
- [x]  Quickly developing and highly efficient
- [ ]  Lengthy paperworks, legal agreements and steep qualifying criteria
- [ ]  None of these





##### DeFi protocols are slower than traditional banks. (T/F)  

- [x]  False

- [ ]  True


    


---
## Use cases of overcollateralized loans

Over-colleteralized borrowing seems to be not relevant initially as the amount of collateral needed to borrow the 
tokens can be quite high. But there are many use cases for it.
* **Yield Farming** - The process involves leveraging DeFi protocols to lend cryptocurrencies for high returns that can 
  go up to 100% APY (Annual Percentage Yield). Yield farming originates from banks’ process in lending your deposits; the difference 
  is that DeFi yield farming compounds the interest earned.

* **Arbitrage** - Arbitrage takes advantage of the fact that an asset may be worth more in one market than another. While 
  this usually happens because of market inefficiencies, it can also be used to exploit differences in rates between 
  different platforms.

* **Margin Trading (Leverage)** - Taking out a loan with extra collateral can help you gain leverage, and you can repeat 
  the process until you reach the limit.

* **Liquidation** - Liquidations can be quite profitable, especially for tech-savvy traders. Usually, a liquidator has to 
  compete against other people for the same job, so he uses bots. They work by "sniping" the loans that are under the 
  collateralization ratio. This way, they can liquidate the collateral and reimburse the lender. In turn, the liquidator 
  receives a reward fee for his services.

* **Risk-reduction/Hedging** - No matter how well you think you know the markets, there will always be bumps in the road. As 
  a trader, you need to find ways to protect your investment from risk, and this is where crypto hedging strategies come in. 
  Hedging encompasses opening positions in opposing market directions to reduce the risks and impacts of market swings. By doing this, 
  you can help to offset any potential losses that might occur.


    


---
## Evaluation





##### What do you mean by Yield Farming?  

- [x]  The process involves leveraging DeFi protocols to lend cryptocurrencies for high returns
- [ ]  It encompasses opening positions in opposing market directions to reduce the risks
- [x]  Returns can go up to 100% APY (Annual Percentage Yield)
- [ ]  Returns do not go above 10% APY (Annual Percentage Yield)





##### Over-collaterization is especially needed in risk reduction of lending which of these?  

- [x]  Volatile assets
- [ ]  Stable assets
- [ ]  Semi-stable assets
- [ ]  None of these





##### Pick the incorrect statements.  

- [x]  Margin Trading involves leveraging DeFi protocols to lend cryptocurrencies for high returns
- [x]  Hedging involves taking out a loan with extra collateral can help you gain leverage
- [ ]  Hedging encompasses opening positions in opposing market directions to reduce any potential losses
- [ ]  Arbitrage takes advantage of the fact that an asset may be worth more in one market than another

    


---
## Borrowing in Aave and Debt Tokenization

We have talked about how we can pay back the loan at any time and that Aave uses something called debt tokenization 
to keep track of our debt. 

## What is debt tokenization? How exactly does it work?

Debt tokenization is like a representation of the debt held in a borrower's name in the form of tokens. When the borrower incurs debt, debt tokens are minted. The debt gets accrued to the debt tokens with interest. The debt tokens are burnt as the debt is repaid.

Now that we have established that users can borrow loans from Aave without any paperwork or minimum criteria.

We know that the loan can be repaid at any time in any quantity, and no extra fees are attached. But what happens when the Health Factor value of the borrow position dips below 1 or the loan starts becoming riskier?

This is handled by Liquidation which is explained in detail in the next step


    


---
## Evaluation





##### What does aave use to keep track of debt?  

- [ ]  Atokens
- [ ]  UNI
- [x]  debtTokens
- [ ]  Both A and B

    


---
## Liquidation in Aave

## Liquidation
The act of selling off collateral in order to cover for debt is called Liquidation. 
It occurs when a borrower's health factor goes below 1 due to their collateral value not properly covering their 
loan/debt value. This might happen when the collateral decreases in value or the borrowed debt increases in value 
against each other. This collateral vs loan value ratio is shown in the health factor (H.F.).

The Health Factor (HF) of a loan needs to stay above one at all times. If the HF falls below one, it means that 
the loan is undercollateralized and the collateral will be liquidated. To bring the HF back up to more than one, 
the collateral is sold off to a liquidity provider with an incentive bonus. The users who pay off the loans and 
buy collateral are called liquidators.

## Preventation of Liquidation

Liquidation is an event triggered by the Health Factor value of loan dipping below 1. 

This can be prevented by two ways.
1. Deposit more collateral into the loan
2. Repay part of the loan such that the H.F. goes comfortably above 1. 

One should be mindful of the token price fluctuations due to market conditions and how it might affect one’s H.F.

## Significance of Liquidation
The system of liquidation is good for those who do the liquidations because they get a significant amount of money 
as a reward. This acts as an incentive to make sure that lenders are provided with safety against loan defaults and 
bad loans. Liquidations are especially useful during bearish markets when viewed from the lender's point of view.


    


---
## Evaluation





##### Collateral is under risk of liquidation when  

- [x]  H.F. < 1
- [ ]  H.F. = 1
- [ ]  H.F. > 1
- [ ]  None of these





##### Can liquidation be prevented?  

- [ ]  No

- [x]  Yes

- [ ]  Sometimes
- [ ]  None of these





##### How can you prevent liquidation?  

- [x]  By repaying part of debt
- [x]  By adding collateral to debt
- [ ]  By borrowing more money
- [ ]  None of these





##### Those who buy collateral with bonuses are called?  

- [x]  Liquidators
- [ ]  Liquidity providers
- [ ]  Liquidity saviours
- [ ]  None of these

    


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
    
