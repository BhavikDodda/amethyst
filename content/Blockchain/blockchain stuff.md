A technology - a decentralized, distributed digital ledger that records transactions across many computers.

> It is a time-stamped series of (immutable) records of data that is managed by a cluster of nodes (computers) not owned by any single entity

(Cryptocurrency)Definition: Adigital currency/token that operates on a blockchain. 

Purpose: Used as money, for paying transaction fees, or as utility tokens (e.g., to interact with dApps). 

Function: Provides incentives for users to maintain the blockchain (e.g., through mining or staking)

# block

1. block number
2. nonce (number used only once)
3. data
4. PH (previous hash)
5. hash (hexadecimal identity)

- Merkle Root: A single hash representing all transactions in the block
- Timestamp: Time when the block was created.

> first block: genesis block

# blockchain ledgers

- private
- public
- consortium/federated: semi-decentralized 

# how it works

- user requests for transaction
- block representing transaction is created
- block is broadcasted
- all nodes validate
- block is added to chain
- transaction gets verified and executed

# distributed consensus

consensus algo:
1. Proof of work
	1. used by bitcoin
2. Proof of Stake
	1. Ethereum 
	2. types
		1. PoS
		2. delegated PoS
		3. Bonded PoS
		4. Nominated PoS
		5. Leased PoS
3. Proof of Authority
4. Proof of Burn
5. Proof of Elapsed Time
	1. made for private blockchain
6. Paxos: Leslie Lamport
	1. Proposer
	2. Acceptor
	3. Learner
7. RAFT: Diego Ongaro
	1. Leader
	2. follower
	3. candidate
8. Practical Byzantine Fault Tolerence: Castro, Liskov
	1. Pre-prepare
	2. prepare
	3. commit

consensus properties:
- agreement
- validity
- fault tolerence

challenges:
- scalability
- latency
- security: defending against 51% attack

# blockchain 2.0

|   |   |   |
|---|---|---|
|Feature|Description|Key Examples / Platforms|
|**Primary Innovation**|**Smart Contracts**|Self-executing code on the blockchain that automatically enforces agreements without needing intermediaries. They are a foundational technology for this generation.|
|**Core Functionality**|**Programmable Platform**|Enables the creation of **Decentralized Applications (dApps)** that run on a decentralized network, not controlled by a single entity.|
|**Key Technology**|**Ethereum Virtual Machine (EVM)**|A runtime environment introduced by Ethereum to execute smart contract code, enabling a massive ecosystem of dApps, DeFi, NFTs, and DAOs.|
|**Asset Representation**|**Tokenization**|Allows for the creation of custom digital tokens to represent various assets, ownership rights, or utility within a system. This is often done using standards like ERC-20 (for tokens) and ERC-721 (for NFTs).|
|**Primary Example**|**Ethereum**|The first major Blockchain 2.0 platform, launched in 2015. Its success led to the development of other platforms aiming for better scalability and features.|
|**Expanded Use Cases**|**Beyond Digital Currency**|Applications extend far beyond simple peer-to-peer payments to areas like Decentralized Finance (DeFi, corda), supply chain management, voting systems (hyperledger), gaming, and digital identity.|

