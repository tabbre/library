---
title: The TabbreChain Whitepaper
date: 2025-01-03
categories: [Blockchain, Crypto]
tags: [jekyll, yaml, markdown]
Author: Charles Cunningham
---
# The TabbreChain Whitepaper

***The multi chain blockchain of the Tabbre Project***



## Introduction

Tabbre's mission is to end the climate crisis and reduce global poverty. Tabbre will achieve these goals by becoming the world's leading supplier of energy by the 2040's. 

All the energy produced and distributed by Tabbre will be carbon neutral and fully sustainable. Tabbre's energy sales will be made in Tabbre's own cryptocurrency, BRE. BRE stands for Basic Renewable Energy.

Tabbre will use the profits from the sale of energy to fund a global universal basic income (GUBI). This will be distributed in BRE.

As a consequence of the scale of Tabbre's energy sales and the distribution of the GUBI, Tabbre will become the world’s de facto self sovereign decentralized global monetary system. Tabbre will supplement and compete with the world’s existing fiat based banking system. Tabbre's BRE currency will provide an independent alternative to the US dollar. This will bring important benefits to the global economy including the ability to run monetary policy for the benefit of the entire world and not just to satisfy the economic needs of one country.

Achieving these goals requires overcoming a number of technical challenges inherent in blockchain technology, including low transaction throughput and a tendency for large decentralized systems to become centralized over time. Tabbre must provide a secure blockchain system that will be able to process millions of transactions per second with low latency and global reach.

 In addition the system needs to accommodate the expected demands of being able to interoperate with the existing fiat currency system and also provide the capability to support DeFi applications. 

It’s with this challenge in mind that Tabbre proposes the integrated multichain system described in this document.

The multichain model that Tabbre proposes consists of a master chain, the TabbChain and a number of dependent sub chains, these will be called BreChain’s.

The Tabbre blockchain system will express two native currencies: TABB and BRE.

TABB will be a fixed supply and hence, deflationary coin that will be used for staking for both the TabbChain and the BreChains.

All coins, both TABB and BRE will be created on the TabbChain. BRE will be transferable to and from the BreChains and between them. These transfers will be conducted using a decentralised transfer service.

## Requirements



### Transactional Throughput
By 2050 the global population will be close to 9.7 billion. 

If the GUBI is payable to everyone on earth, and each person is allocated an account at birth, this implies 9.7 billion accounts. 


If we assume 10 transactions a day for these accounts, this implies a transactional rate of 1.1 million transactions per second. 

### Interoperability

The Tabbre blockchain system will need to be interoperable with the existing global financial system. The key to this interoperability lies in the metadata associated with transactions. Metadata describes the who, where,when and why of transactions. 

Current blockchain systems do not collect this information.

### Decentralization
As decentralized ledgers grow in size the cost involved with running a node increases. This has a consequence that the number of independent node operators declines resulting in a reduction in decentralization. The Tabbre blockchain needs to be adequately decentralized to preserve the benefits of decentralization while delivering the service performance needed for a truly global financial system.



## Tabbre’s Approach to Scalability

The lack of scalability is a major concern for blockchain developers. Various approaches have been tried, all come up short. The problem of blockchain scalability in terms of transactional throughput is typically presented as a trilemma, where only two out of the following three alternatives can be had: 

- High transaction throughput

- Security
- Decentralization

All current efforts to provide a high transactional throughput seem to sacrifice either security or more typically decentralization. Some achieve modest improvements in transactional throughput over the established decentralized blockchains by optimising existing design practice without sacrificing either security or decentralization. The Tabbre project takes advantage of this work.

The root cause of the trilemma is the fact that the consensus process for replicated state machines at the heart of the blockchain decentralized ledger is fundamentally single threaded.

The trilemma can never be solved for a single blockchain. The best that can be achieved is an optimized design that will allow something like a thousand transactions per second. This is two or three orders of magnitude better than the early blockchain designs, but is still orders of magnitude too small for a globalized system that will require millions of transactions per second.

Tabbre proposes to solve the problem of scalability by the simple expedient of introducing many blockchain ledgers, each of identical design and operation, each operating their own independent consensus and each expressing the same currency. Tabbre calls this architecture a Multichain Ledger. 

Transfers of value between blockchains will be relatively infrequent. An amount of coin on one Tabbre Multichain blockchain is worth the same as the same amount of coin on any other Tabbre Multichain blockchain. 
Transfers to accounts will create the account if it doesn’t already exist. A user’s account balances can exist on any number of Tabbre Multichain blockchains. 
End users will not see the individual blockchains, their experience will be simplified by wallets that provide an aggregate view of an account, all balances for an account that exist on every blockchain in the ledger will be displayed as a single account balance by the wallet.

The Tabbre Multichain approach is conceptually simple and delivers increased throughput.
$$
tx/s = Number Of Transactions Per Second
$$
$$
tx/b = Number Of Transactions Per Block
$$
$$
b/s	= Block Rate Per Second
$$
$$
N	= Number Of Blockchains In Multichain
$$



For all existing blockchains:

Transaction rate per second     =  (Number of Transactions per block)  x (Block Rate Per Second) 

or: 
$$
tx/s  	 = (tx/b) . (b/s)
$$
For Tabbre Multichain: 

Transaction rate per second    =  (Number of Transactions per block) x (Block Rate Per Second) x (Number of blockchains)



or: 
$$
tx/s  	 = (tx/b) . (b/s) . N
$$
This approach means that the Tabbre Multichain architecture is linearly scalable: each blockchain requires the same processing power as any other blockchain in the multichain ledger and the more blockchains that exist in the multichain the more transactional throughput is available.
Adding more blockchains proportionately adds more throughput.

## How the Tabbre Multichain ledger works

The Tabbre Multichain protocol provides a mechanism for sharding a blockchain based distributed ledger and in so doing addresses the problem of scalability that afflicts blockchain systems. The Tabbre Multichain scheme provides for near linear scalability, the more shards that are added together with proportionately more processing power, the correspondingly more transaction throughput.


In the Tabbre Multichain system the shards are referred to as subchains and the complete Tabbre Multichain ledger that consists of the subchains is termed a multichain. 


Each subchain is a self contained blockchain based replicated database with its own replication consensus and works independently of any other subchain. All subchains are equally secure.



+++++++++++++++++

### Scale

1. Global distribution

2. 9 billion accounts

3. At 10 Tx per account per day => c. 1 million tps 

4. 1 second blocktime
5. TX data 256bytes => 2.5Kbits per tx

### Blockchain Implications

Each blockchain: 10,000 tps =>  100x blockchains

If blockrate is 1 per second and each Blockchain has 1000 validator nodes => 100,000 validators



### Network constraints

Earth 40,000 km in circumference

Speed of light in fibre optic cable 200,000 Km per second

Latency 1 ms per hop

Assume max 20 hops and 80,000 km round trip => 80/200 seconds + 20 ms => 420ms latency


=> blockrate of c. 2  per second for a global system

If finality is assumed after 12+ blocks (like Ethereum), the transaction finality will be 6 seconds.

### Network traffic

Each node receives and sends all Tx data 2x

Tx data per second = 256 x 2 x 10 bits * 10,000 = 51.2*106   bps or c. 50 mbps.



# **Data Storage volumes**

Each node receives and sends all Tx data 2x

Tx data per second = 256 x 2 x 10 bits * 10,000 = 51.2*106  bps or c. 50 mbps.

Storage capacity: if each TX is 2k bytes => 20 MBytes per second. => 6.3x1014

Providing for 100% redundancy => c. 1.2 Petabytes pa.

# **Costs**

## **Network** 

Gigabit Ethernet costs c. $500/£300 pcm

## **Data Storage**

Cost today for storage at retail prices: $40,000 per petabyte => $48,000

## **Processing Power**

Rack mounted servers; $30,000 USD

Energy cost assuming 2 Kw consumption at $0.3 per KWh => c. $5256 pa

Estimated cost of running nodes at today's prices => c. $100,000

# **Cost of running Tabbre multichain**

Number of blockchain nodes = 100,000

Annual cost of running a validator = $100k =

Cost of running Tabbre network => $10bn pa.

# **Revenue**

At $0.01 per Tx => ($0.01 per tx) x (106 x seconds per year) = $315 bn

# **Economics**

Tabbre Project estimated total capex = $15 tr.

Project Duration - years	15 

Avg spend pa $ 1.0 tr pa

Average running cost = 1% of installed capital

Max spend 10% total capex = $1.5 

Capex avg life years

Tabbre Revenue in 2045 in 2023 USD = $4.5 tr pa 

Interest Rate	= 5%

Zero coupon discounted bonds maturing in 10 years

# **How much will TABB be worth?**

2045 ESTIMATE

If Tabbre Revenue = $4.5 tr pa and this is 90% profit and we assume a PE of 25

TABB will be worth $100 tr







## Architecture





![](https://raw.githubusercontent.com/tabbre/library/35a5859cab652bdf9afab207cdee1557441f5bc1/images/Diagrams/Tabbre%C2%A0Wallet%20Service%20Provider%20Architecture.svg)

The TabbreChain will be a proof of stake (PoS) secured blockchain. 

The TabbreChain is a dual currency blockchain, expressing both TABB and BRE coins. TABB being the required currency for the staked deposits. 

TabbreChain transaction charges will be payable in BRE. The block sealing rewards payable to block validators will be paid in BRE.

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



