## Header
This is the course header. This will be added on top of every page. Go to [DoDAO.io](https://www.dodao.io) to know more.

---

## Flash Loans


## What are flash loans?

Flash loans are special transactions that allow you to borrow an asset and return it within a single transaction. 
They're also known as block borrows. Flash loans don't require any collateral to function. That's because they're 
made up of the words "flash," which means fast or instant, and "loan," which can be understood by the traditional 
finance terminology.

Flash loans are essentially like short-term loans that are codified by smart contracts. This means that the terms 
of the loan are written in code, which helps to prevent funds from being transferred out of one account to another 
unless certain conditions have been met. Flash loans are typically repaid in the same transaction, and they are 
only valid for as long as the liquidity remains in the pool. However, if a flash loan trade doesn't return the full 
amount of liquidity to the pool, the entire transaction will be reversed, which will also reverse all previous 
actions. This helps to ensure that funds are safe during a transaction.


    


---
## Evaluation





##### What do Flash loans mean?  

- [ ]  Slow loan processing without collateral.
- [ ]  Instant loan processing with collateral
- [ ]  Slow loan processing with collateral.
- [x]  Instant loan processing without collateral.





##### A flash loan can extend to how many transactions?  

- [x]  1
- [ ]  2
- [ ]  5
- [ ]  10

    


---
## What is a Transaction in Ethereum

A transaction is a way of transferring value or any other type of token using Ethereum. In order to transfer 
cryptocurrency, you must have a digital wallet. This wallet must have a public and private key. You can think of 
it like this: your wallet is your bank account, your public key is your account number, and your private key is 
your pin code.

Once you have connected your wallet, you can use various decentralized exchanges and decentralized finance 
platforms to complete transactions. On every transaction, a fee is added, which acts as an incentive to miners 
to keep the chain secure. 

Users can perform various tasks like lending, borrowing, transferring and converting currencies using blockchain.

But have you ever imagined? Taking a loan without any colleteral, utilizing it and then returning it back in the 
same transaction? That's what Flash Loans are.


    


---
## Evaluation





##### What is the collateral amount needed to get a flash loan?  

- [x]  No collateral
- [ ]  10%
- [ ]  125%
- [ ]  25%

    


---
## Working of Flash Loan

Aave V3 offers two options for flash loans:

  * `flashLoan`: Allows borrower to access liquidity of _**multiple reserves**_ in single _flashLoan_ transaction. The borrower also has an option to open stable or variabled rate debt position backed by supplied collateral or credit delegation in this case.\
  NOTE: _flash loan fee_ is waived for approved `flashBorrowers` (managed by ACLManager)
  
  * `flashLoanSimple`:  Allows borrower to access liquidity of _single reserve_ for the transaction. In this case flash loan fee is not waived nor can borrower open any debt position at the end of the transaction. This method is gas efficient for those trying take advantage of simple flash loan with single reserve asset.

### Execution Flow

For developers, a helpful mental model to consider when developing your solution:
  
  1. Your contract calls the `Pool` contract, requesting a Flash Loan of a certain `amount(s)` of `reserve(s)` using `flashLoanSimple()` or `flashLoan()`.
  2. After some sanity checks, the `Pool` transfers the requested `amounts` of the `reserves` to your contract, then calls `executeOperation()` on `receiver` contract .
  3. Your contract, now holding the flash loaned `amount(s)`, executes any arbitrary operation in its code.&#x20;
  * If you are performing a **flashLoanSimple**, then when your code has finished, you approve Pool for flash loaned amount + fee.
  * If you are performing **flashLoan,** then for all the reserves either depending on  `interestRateMode` passed for the asset, either the Pool must be approved for flash loaned amount + fee or must or sufficient collateral or credit delegation should be available to open debt position.
  * If the amount owing is not available (due to a lack of balance or approvaln or insufficient collateral for debt), then the transaction is reverted.
  4. All of the above happens in 1 transaction (hence in a single ethereum block).


    


---
## Evaluation





##### What are the two differents methods which can be called to get Flash Loans?  

- [x]  `flashLoanSimple`
- [ ]  `doFlashLoan`
- [x]  `flashLoan`
- [ ]  `instantLoan`





##### Which method is called on the receiver contract for Flash Loan?  

- [ ]  `useFlashLoan`
- [ ]  `executeLoan`
- [ ]  `executeFlashLoan`
- [x]  `executeOperation`

    


---
## Code using Flash Loan

```solidity
  /**
  !!!
    Never keep funds permanently on your FlashLoanSimpleReceiverBase contract as they could be
    exposed to a 'griefing' attack, where the stored funds are used by an attacker.
  !!!
  */
  contract MySimpleFlashLoanV3 is FlashLoanSimpleReceiverBase {
    using SafeMath for uint256;
  
    constructor(IPoolAddressesProvider _addressProvider, IFaucet _faucet) FlashLoanSimpleReceiverBase(_addressProvider, _faucet) {}
  
    /**
    This function is called after your contract has received the flash loaned amount
    */
    function executeOperation(
      address asset,
      uint256 amount,
      uint256 premium,
      address initiator,
      bytes calldata params
    )
    external
    override
    returns (bool)
    {
    
      //
      // This contract now has the funds requested.
      // Your logic goes here.
      //
      
      // At the end of your logic above, this contract owes
      // the flashloaned amounts + premiums.
      // Therefore ensure your contract has enough to repay
      // these amounts.
      
      // Approve the LendingPool contract allowance to *pull* the owed amount
      uint amountOwed = amount.add(premium);
      FAUCET.mint(asset,premium);
      IERC20(asset).approve(address(POOL), amountOwed);
      
      return true;
    }
  
    function executeFlashLoan( address asset, uint256 amount) public {
      address receiverAddress = address(this);
      
      bytes memory params = "";
      uint16 referralCode = 0;
      
      POOL.flashLoanSimple(receiverAddress, asset, amount, params, referralCode);
    }
}
```
This code can be found at [https://github.com/defispartan/hackmoney-demo](https://github.com/defispartan/hackmoney-demo)


    


---
## Applications of Flash Loans

#### Arbitrage 
Users can earn a decent profit by trading assets at different platforms that offer different values. For example, 
users can buy crypto from one exchange and sell it on another with varying rates and make a profit doing so.

With flash loans, traders can launch an arbitrage without any existing assets. When a price difference is found, 
traders can instantly borrow a considerable amount of money using a flash loan service. Therefore, arbitrage trades 
using a flash loan become "cost-free" as long as the traders can afford the gas and flash loan fee to launch the 
transaction.


#### Swapping Collateral    
Crypto asset investors can use collateral swapping to change out their investments without having to repay the 
debt of the original investment. This can be important in a volatile market where timing is key to avoiding 
liquidation. Collateral swapping lets an investor replace their position with borrowed assets.

Users can choose to pay back their CDP debt and take out all collateral, using part of it to repay flash loans 
and keeping the remaining for themselves.

#### Self Liquidation

Markets can be very volatile and can lead liquidation of the sensative positions. Liquidation can be quite expensive
on certail platforms, and it might make sense to write a simple script to self-liquidate your loans using flash 
loans and your own deposit to pay them back.

There are many applications that make use of flash loans and liquidate the positions on user's behalf saving the 
user hefty liquidation fees of the protocol.


    


---
## Evaluation





##### How does DeFi solve the volatility of cryptocurrency?  

- [ ]  Using smart contracts
- [x]  Using Stablecoins
- [ ]  Using Flash Loans
- [ ]  None of these





##### Which one is not a use case of Flash Loan?  

- [ ]  Flash Minting
- [ ]  Collateral swapping
- [x]  Slow loan processing
- [ ]  Wash-trading

    


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
    
