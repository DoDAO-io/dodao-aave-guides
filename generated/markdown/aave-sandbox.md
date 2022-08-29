## Header
This is the course header. This will be added on top of every page. Go to [DoDAO.io](https://www.dodao.io) to know more.

---

## AAVE Sandbox


## Aave Sandbox

### Aave Sandbox

Aave sandbox is a GitHub repository that replicates the forked production environment.The environment is 
envisioned for testing liquidations and other integrations that require a production state using hardhat node and alchemy.

See here - https://github.com/aave/aave-sandbox


### Setting up the environment:

1. Set up a code editor like VScode and install node js and git.
2. Clone repository using git clone [https://github.com/aave/aave-sandbox.git](https://github.com/aave/aave-sandbox.git)
3. Install npm i (type npm i in the terminal for installation).
4. Create a .env file.(touch.env)
5. Create an alchemy key from the alchemy website

What is a Hardhat node?

Hardhat is a framework for testing, running, and deploying smart contracts and scripts in the blockchain. It features clear error messages, 
forking the mainnet and other networks, mining nodes, logging, etc.

Hardhat Network has the ability to copy the state of the mainnet blockchain into your local environment, including all balances and deployed contracts. 
This is known as the "forking mainnet."


    


---
## Evaluation





##### What are the tools we are using for aave sandbox?  

- [ ]  Ganache
- [x]  Hardhat
- [x]  Alchemy
- [ ]  Truffle





##### What are requirements we need to install for forking?  

- [x]  Npm and Hardhat
- [ ]  Alchemy API key and nodejs
- [ ]  Truffle
- [ ]  None of these





##### Which of the following is correct about Aave sanbox?  

- [ ]  Sandbox is framework for deploying and testing smart-contracts
- [x]  Sandbox is a github repository that replicates the forked production environment.
- [ ]  Sandbox is a smartcontract for Aave
- [ ]  None of these

    


---
## Forking Aave markets


###Forking Aave V3 markets.

For forking, we need to complete the installation of npm and hardhat.Now clone the Aave sandbox repository or use 

```
git clone https://github.com/aave/aave-sandbox.git
```

After cloning the repository, create an Alchemy API key from the alchemy website. Store the alchemy key in the created .env file, as shown below.

```
# Content of .env file
ALCHEMY_KEY=your-alchemy-key
```
Note: Dont share your API key and mention the .env file in the gitignore so that it wont be pushed.

If you want to integrate any deployed Aave V3 markets, you can spin a sandbox node in the following way.
In a separate window, run the sandbox Hardhat fork node that will be reachable via JSON RPC at `http://127.0.0.1:8545/`. 
You can spin the sandbox node with the following command, replacing "polygon" with the desired chain:

```
npm run node:fork:polygon-v3
```


Now you can connect to the Hardhat Node via JSON RPC at `http://127.0.0.1:8545/` in your project and use official deployed addresses to 
interact with the market. Once the node runs, the following tasks will point to the sandbox node.
Tasks like feed-account,print-balance,print-accounts,etc. It will be useful for analyzing the market.

If you need the official ERC20 tokens in the sandbox environment, you can get ERC20 tokens using the `feed-account` task. 
The task will override the balance of the address via `hardhat_setStorage`.
You can use the following command as a faucet to get all ERC20 tokens used inside a market.


```
npm run feed-accounts:polygon-v3 --accounts 0x976EA74026E726554dB657fA54763abd0C3a0aa9,<other-user-address>
```


    


---
## Evaluation





##### Where should we store the alchemy key?  

- [ ]  in the created variable ALCHEMY_KEY
- [ ]  we need to store in the contracts
- [x]  We need to store in the environment variable which we have created as .env
- [ ]  we dont use API keys





##### How to connect the forked chain to the Hardhat node?  

- [x]  We need to edit the hardhat config file and set the requirements for the connecting it with the forked market.
- [ ]  We can use command connect hardhat for connecting it.
- [ ]  we wont connect it.
- [ ]  None of these





##### How to get the official ERC-20 tokens in the sandbox node?  

- [ ]  we can get it by using smart-contracts
- [ ]  We can get it by connecting our wallet to a faucet
- [x]  We need to use the feed-account task.
- [ ]  None of these

    


---
## Aave arc sandbox

###Aave arc sandbox

In a separate window, run the sandbox Hardhat node that will be reachable 
via JSON RPC at `http://127.0.0.1:8545/`. You can spin the sandbox node with the following command:

```
npm run node:fork:arc
```
Once the node is running, the following tasks will point to the sandbox node. You can also point your project to target the sandbox node.
To add liquidity to the Aave Arc, proceed to feed liquidity and create possible liquidable positions:

```
npm run feed-market:arc
```
Once there is liquidity at the market, you can view the users balance and possible liquidable positions with the following command:

```
npm run print-accounts:arc
```
Output:
User Info:
- Address: 0x976EA74026E726554dB657fA54763abd0C3a0aa9
- Health Factor:  0.918421511765627487
- Balances
┌─────────┬───────────────────┬───────────────────┬──────────────────────────┬────────┐
│ (index) │ enabledCollateral │ collateralBalance │       debtBalance        │ symbol │
├─────────┼───────────────────┼───────────────────┼──────────────────────────┼────────┤
│    0    │       true        │     '50000.0'     │          '0.0'           │ 'USDC' │
│    1    │       false       │       '0.0'       │          '43.0'          │ 'WBTC' │
│    2    │       false       │       '0.0'       │ '543.999999948668340512' │ 'WETH' │
│    3    │       true        │     '50000.0'     │          '0.0'           │ 'AAVE' │
└─────────┴───────────────────┴───────────────────┴──────────────────────────┴────────┘
[...]



For whitelisting your accounts or smart contracts like liquidation bots into Aave Arc Sandbox, you can use the following command:

```
whitelist-accounts:arc --accounts <your-account-address>,<your-smart-contract-address>
```
Now you can connect your project to the Hardhat Node via JSON RPC at `http://127.0.0.1:8545/` in your project and use official 
deployed addresses to interact with the market.


    


---
## Evaluation





##### How to view the user's and markets information after forking?  

- [ ]  We need to create a smartcontract and ask for the details required
- [x]  We can use the tasks which was defined in the sandbox repo to analyse and view market.
- [ ]  Use can view it by using the command in the terminal give users info.
- [ ]  We cannot view users and market information after forking.





##### Which of the following command is correct about adding liquidity to the Aave arc?  

- [ ]  npm run node:fork:arc
- [x]  npm run feed-market:arc
- [ ]  npm run print-accounts:arc
- [ ]  npm run node:fork:polygon-v3





##### How to view the user's and markets information after forking?  

- [ ]  We need to create a smartcontract and ask for the details required
- [x]  We can use the tasks which was defined in the sandbox repo to analyse and view market.
- [ ]  Use can view it by using the command in the terminal give users info.
- [ ]  We cannot view users and market information after forking.

    


---
## Forking Aave v2 main

###Aave V2 Main

If you want to integrate the permissionless Aave market, you can also spin a sandbox in the following way.
In a separate window, run the sandbox Hardhat node that will be reachable via JSON RPC at `http://127.0.0.1:8545/`. You can spin the sandbox node 
with the following command:

```
npm run node:fork:main-v2
```

Now you can connect to the Hardhat Node via JSON RPC at `http://127.0.0.1:8545/` in your project and use official deployed addresses to interact with the market.
Once the node runs, the following tasks will point to the sandbox node.To add liquidity to the Aave Main market, proceed to feed liquidity and create possible liquidate positions:

```
npm run feed-market:main-v2
```

View users positions at the Main market and possible liquidable positions, but only limited to a subset of addresses passed by the argument `--accounts`:

```
npm run print-accounts:main-v2 -- --accounts 0x23618e81E3f5cdF7f54C3d65f7FBc0aBf5B21E8f,0x14dC79964da2C08b23698B3D3cc7Ca32193d9955
```
###Utilities        
**Enable mining by interval**

By default Hardhat node mines block every time you perform a transaction, but for some scenarios you may need the node to mine blocks by interval.
You can enable Hardhat to mine blocks every 5 seconds with the following command:
```
npm run set-interval-mining
```
To disable mining empty blocks, you can run:

```
npm run set-interval-mining: off
```


    


---
## Evaluation





##### Which of the following is correct command for forking Aave mainnet market?  

- [ ]  npm run feed-market:main-v2
- [x]  npm run node:fork:main-v2
- [ ]  npm run set-interval-mining
- [ ]  hardhat --fork:mainnet





##### Which of the following is correct about seeting interval for mining the blocks?  

- [x]  npm run set-interval-mining
- [ ]  npm run node:fork:main-v2
- [ ]  npm set interval [5]
- [ ]  hardhat set interval --block

    


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
    
