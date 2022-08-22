## Header
This is the course header. This will be added on top of every page. Go to [DoDAO.io](https://www.dodao.io) to know more.

---

## Decentralized Borrowing


## Important terms


Decentralized borrowing refers to the the process of borrowing assets from Decentralized finance. In order to understand 
its workings and uses, we need to know a few of these important terms first.

- **Liquidation:**
The selling of collateral to cover the debt is called liquidation.

- **LTV (Loan to Value):**
Loan to value is the ratio used to decide how much loan can be borrowed against the collateral produced. It is expressed in terms of percentages. (e.g., at LTV=75%, for every 1 ETH worth of collateral, borrowers will be able to borrow 0.75 ETH worth of the corresponding currency). 

- **Liquidation Threshold:**
The liquidation threshold is the percentage at which a loan is deemed undercollateralized. For example, a Liquidation threshold of 70% means that if the loan's value rises above 70% of the collateral, the position is undercollateralized and could be liquidated.

- **Liquidation Penalty:**
The liquidation penalty is a fee rendered on the price of assets of the collateral when liquidators purchase it as part of the liquidation of a loan that has passed the liquidation threshold.

- **Health Factor:**
It is a risk parameter that decides whether a borrow position is at risk of getting liquidated. It is calculated by,

( H.F = ΣCollateral in ETH x Liquidation threshold / Total borrows )


    


---
## Evaluation





##### Which parameter decides the risk of an loan's liquidation?  

- [x]  Health Factor
- [ ]  Liquidation penalty
- [ ]  LTV
- [x]  Liquidation threshold





##### The selling of collateral to cover for debt is?  

- [ ]  Health Factor
- [ ]  LTV
- [x]  Liquidation
- [ ]  None of these





##### LTV stands for  

- [x]  Loan to Value
- [ ]  Load to vector
- [ ]  Loading the value
- [ ]  None of these





##### The percentage at which a loan is deemed undercollateralized:
  

- [ ]  LTV
- [ ]  Liquidation percentage
- [x]  Liquidation threshold
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





##### Which of these borrowing options is costlier  

- [ ]  Traditional loan
- [x]  DeFi loan
- [ ]  Both of these
- [ ]  None of these





##### The features of Traditional finance are:
  

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

- **Credit enchancement:**
Traditionally, overcollaterization is used as a credit enhancement technique, That is it is used as a means of risk-reduction to the lender in case of financial stress. By overcollaterization, credit risk is eliminated; The lender could liquidate the collateral to recover any possible loan losses.
This also works in the borrowers favor. With the increased security provided to the lender, The borrower is put in a position where they can negotiate for a better interest offer on the loan.

- **Security:**
Overcollaterization comes to the rescue when dealing with highly volatile assets like cryptocurrencies. In case the value of the collateral dips beyond the actual value of the loan taken, Then the lender’s assets are compromised. To prevent this, DeFi organizations set the percentage of overcollateralization. In case the value of the collateral dips beyond a certain point, It is liquidated and the position of the lender is secured.

- **Buffer:**
An overcollateralized stablecoin has a large number of cryptocurrency tokens maintained at a reserve for issuing a lower number of stablecoins. This offers a buffer against price fluctuations.

- **Leverage:**
Leveraging interest rates of currency taken loan against and invested in. 

- **Liquidity Generation:**
Another simple use case would be liquidity. You just generated liquidity without losing hold of your cryptocurrency by borrowing a loan with it as collateral.

- Overcollateralization is a common practice in securitized financial products like Collateralized loan obligations (CLO) and Mortgage Backed Securities (MBO). 


    


---
## Evaluation





##### Overcollateralization is a common practice in:
  

- [ ]  CLO
- [ ]  MBO
- [x]  Securitized financial products
- [ ]  All of these





##### In what way is overcollateralization beneficial?  

- [x]  Liquidity
- [x]  Leveraging
- [x]  For favourable loan terms
- [ ]  To spend excess assets





##### Traditionally, over-collateralization is used as?  

- [x]  Credit enhancement technique
- [ ]  Credit producing technique
- [ ]  Credit advancement technique
- [ ]  None of these





##### Over-collaterization is especially needed in risk reduction of lending which of these?  

- [x]  Volatile assets
- [ ]  Stable assets
- [ ]  Semi-stable assets
- [ ]  None of these

    


---
## Borrowing in Aave and Debt Tokenization

Aave uses debt tokenization to keep track of debt accumulated by the borrower.

## What _is_ debt tokenization? How exactly does it work?

Debt tokenization is like a representation of the debt held in a borrower's name in the form of tokens. 
When the borrower incurs debt, debt tokens are minted. The debt gets accrued to the debt tokens with interest. 
The debt tokens are burnt as the debt is repaid.

## Process of borrowing in Aave



*     Before borrowing, the users must put forward collateral. The LTV of each coin is different. For stablecoins, LTV is generally higher, while LTV is a bit lower for more volatile assets. Since the probability of the value of a more volatile coin dipping is higher, this is done to protect the lender's position in case of liquidation.

    **Note:** All assets are borrowed upon over-collateralization.

* You can find the crypto you wish to borrow on the Aave page once you are done paying collateral.
* Click "borrow" on the right of the screen.
* The user is then prompted to connect their web 3.0 digital wallet. Once connected, choose the amount you would like to borrow.
* The website has options for stable interest rates and variable interest rates.
* Choose the preferred interest rate and confirm the transaction through your web 3.0 digital wallet.

## Changes in Aave 2.0
 * Borrowers can swap between variable and stable interest rates, which means the user can get the best possible interest rate offer at any given time.

 * Collateral deposited before borrowing funds can now be swapped for another cryptocurrency inside Aave. 

 * You can now directly repay debt using collateral. In V1, they will first need to withdraw the collateral, use it to buy the asset borrowed, then finally repay the debt and unlock all the deposited collateral. This operation costs time and requires, at best, four separate transactions on several protocols.

 * Anyone can trade their debt position from one asset to another natively. You could, for example, borrow DAI and change your debt position to USDC as soon as USDC becomes cheaper to borrow, all of this within a single transaction.


    


---
## Evaluation





##### Overcollateralization in normal DeFi borrowing is?  

- [x]  Mandatory
- [ ]  Never used
- [ ]  Sometimes used
- [ ]  None of these





##### The function of Debt tokens is?  

- [x]  To keep count of the interest on debt for a given address/user
- [ ]  To keep count of the interest on deposited money for a given address/user
- [ ]  To be used in voting for changes in the protocol
- [ ]  None of these





##### What does aave use to keep track of debt?  

- [ ]  Atokens
- [ ]  UNI
- [x]  debtTokens
- [ ]  Both A and B





##### You can find the crypto you wish to borrow on the Aave page once you are done doing?  

- [ ]  Interest rate decision
- [ ]  Logging on to Aave
- [x]  Paying collateral
- [ ]  None of these

    


---
## Interest rates in Aave



    


---
## Evaluation





##### By what percentage can the staked AAVE tokens of the token holders be slashed incase of a liquidity crisis?  

- [x]  30%
- [ ]  50%
- [ ]  80%
- [ ]  10%





##### The Aave token holders are incentivized in return for which of the following?  

- [ ]  For approving the governance proposals
- [ ]  For proposing AIPs and voting
- [x]  For bearing the risk of the protocol i.e. by staking
- [ ]  None of these





##### By what percentage can the staked AAVE tokens of the token holders be slashed incase of a liquidity crisis?  

- [x]  30%
- [ ]  50%
- [ ]  80%
- [ ]  10%





##### The Aave token holders are incentivized in return for which of the following?  

- [ ]  For approving the governance proposals
- [ ]  For proposing AIPs and voting
- [x]  For bearing the risk of the protocol i.e. by staking
- [ ]  None of these

    


---
## Liquidation in Aave

## Liquidation
The act of selling off collateral in order to cover for debt. 
Liquidation is a process that occurs when a borrower's health factor goes below 1 due to their collateral value not properly covering their loan/debt value. 
This might happen when the collateral decreases in value or the borrowed debt increases in value against each other. 
This collateral vs loan value ratio is shown in the health factor (H.F.).

The Health factor of a loan ( i.e., H.F. = ΣCollateral in ETH x Liquidation threshold / Total borrows ) should be maintained above one by the borrower at all costs.
This is because if the H.F. drops below 1, The collateral is bound to be liquidated because H.F. less than one indicates that the loan is undercollateralized. 
So the collateral is liquidated, and a part of the loan is paid off to bring the H.F. back to more than 1. 
The collateral is sold off to a liquidity provider with an incentive bonus. T
The users who pay off the loans and buy collateral are called **liquidators**.

## Preventation of liquidation
Liquidation is an event triggered by the H.F. value of loan dipping below 1. 
This can be prevented by two ways.
1. Deposit more collateral into the loan
2. Repay part of the loan such that the H.F. goes comfortably above 1. 

One should be mindful of the stablecoin price fluctuations due to market conditions and how it might affect one’s H.F.

## Significance of Liquidation
The current system of liquidation is beneficial for those who perform the liquidations. They are given a significant amount of money as a reward, which acts as an incentive.
This ensures that the lenders are provided with safety against loan defaults and bad loans, though the loan might be overcollateralized, without liquidators to buy the collateral, the excessive collateral just sits there idly.
Liquidations come very handy in bearish markets from the lender point of view.


    


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
    
