# The TabbChain



## Introduction

If Tabbre is to achieve its goal of becoming a self sovereign global reserve currency system, Tabbre must overcome the challenge of providing a secure blockchain system that will be able to process millions of transactions per second with low latency and global reach. In addition the system needs to accommodate the expected demands of being able to interoperate with the existing fiat currency system and also provide the capability to support DeFi applications. It’s with this challenge in mind that Tabbre proposes the  integrated multichain system described in this document.


The multichain model that Tabbre proposes consists of a master chain, the CoreChain and a number of dependent sub chains, these will be called BreChain’s.


The Tabbre blockchain system will express two native currencies: TABB and BRE.


TABB will be a fixed supply and hence, deflationary coin that will be used for staking for both the CoreChain and the BreChains.


All coins, both TABB and BRE will be created on the CoreChain. BRE will be transferable to and from the BreChains and between them. These transfers will be conducted using a decentralised transfer service.

## Requirements

### Scale

1. Global distribution

2. 9 billion accounts

3. At 10 Tx per account per day => c. 1 million tps 

4. 1 second blocktime

5. TX data 256bytes => 2.5Kbits per tx

## Architecture





![](https://raw.githubusercontent.com/tabbre/library/35a5859cab652bdf9afab207cdee1557441f5bc1/images/Diagrams/Tabbre%C2%A0Wallet%20Service%20Provider%20Architecture.svg)

The TabbChain will be a proof of stake (PoS) secured blockchain. 

The TabbChain is a dual currency blockchain, expressing both TABB and BRE coins. TABB being the required currency for the staked deposits. 

Tabbre Chain transaction charges will be payable in BRE. The block sealing rewards payable to block validators will be paid in BRE.

The rules governing the operation of the TabbChain staking mechanism will be managed by smart contracts.

Validator nodes (validators) will compete to seal blocks on the blockchain. A validator asserts that all the transactions recorded in the block are both fully valid and verified. If a block contains a transaction or transactions that are disputed by another validator then the block can be discarded if a quorate majority of validators agrees that the block should be discarded and replaced by a block that doesn’t contain the disputed transaction(s). 

If this happens the validator of the rejected block will suffer a confiscation of a fraction of their staked TABB. The possibility of staked TABB being confiscated provides the economic incentive to keep validator operators honest. This is based on the assumption that the economic gain from approving dishonest transactions is always less than the cost of having a stake confiscated.

The security of a proof of stake blockchain is therefore a function of the ratio of transactional value to staked value.

TABB will be a deflationary cryptocurrency, with a fixed maximum supply. Demand for TABB will be driven in part by the Proof of Stake model of the Tabbre Chain as well as the use of TABB as collateral for the issuance of BRE denominated credit. As the value of assets held on the Tabbre Chain increases so too will the value and quantity of transactions increase. This will result in the BRE denominated rewards and fees paid to node operators also increasing.

This will attract new node operators who will need to stake TABB, creating a demand for TABB. 

As the value represented by assets on the Tabbre Chain increases the total value of TABB staked will also increase to maintain the security of the blockchain. This may lead to the size of the deposited staked funds required to operate a Tabbre Chain node increasing, however the total value of TABB staked can also increase through the effect of more nodes joining the network and also through an increase in the market value of TABB.



### **Security is based on the relative value of TABB** {#security-is-based-on-the-relative-value-of-tabb}



![](https://github.com/tabbre/library/blob/main/images/Diagrams/TABB%20Staking.png?raw=true)

Once mature, the Tabbre Project will use the income arising from the sale of energy either to bolster the scheme's reserves or else it will be distributed.  
The preferred distribution method is for the Tabbre Project to buy TABB in the open market.  
The purchased TABB may either be  held or burnt.  
This links the sale of energy to the crypto economic model protecting the consortium blockchain.  
As the Tabbre Projects energy sales increase  so too will the issuance of BRE increase over  time, so will the Tabbre Project’s income that can be used  to purchase  TABB.  
This will drive both the demand for TABB and increase the scarcity of TABB.  
Hence increasing TABBs value and so increasing the value of the capital deployed to secure the TabbreChain blockchain, making it correspondingly more secure.  
Validator node operators will  be rewarded for operating their nodes: the BRE collected as transaction charges will be paid to the operators of validator nodes.  
As the scheme grows in size so will the transaction charge revenue collected.  
This will also drive demand for TABB and hence the price of the TABB.