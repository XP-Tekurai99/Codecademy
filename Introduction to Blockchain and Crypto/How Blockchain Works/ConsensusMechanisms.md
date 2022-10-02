# Consensus Mechanisms

## Learning Objectives
The different consensus mechanisms and how they work.

## Consensus Mechanism Types
The mining process requires miners to perform work using an external resource (energy) to actually “mine” and create new units of cryptocurrency. This method is specific to a Proof of Work (PoW) blockchain like Bitcoin, but there are other consensus mechanisms.

Other consensus mechanisms, like Proof of Stake, aim to provide the data verification of a PoW chain without the same energy needed. This has certain use cases, but it has important tradeoffs developers need to be aware of.

We’ll go over those so we can make an informed decision about what kind of blockchain we want to build on.

### Proof of Work
Proof of Work (PoW) is the consensus mechanism used by Bitcoin. It involves utilizing a large amount of computing energy to solve a complex cryptographic puzzle to win the privilege of mining a new block. We must “prove” we’ve done the “work” to earn the reward of a new block.

A gif showing how Proof of Work works. It takes a hash, adds difference nonces to it, calculates the SHA-256 hash, and keeps doing this until a valid hash is found.

There are two critical things to keep in mind with PoW:

This consensus mechanism relies on external input. It requires using one valuable resource (energy) in order to produce another (Bitcoin).
A common criticism of PoW is this large energy usage. This is often described as a weak point and a disadvantage, but it’s important to understand why it is a feature, and not a bug, of PoW that it uses so much energy.
Proof of stake
As an answer to PoW’s large energy usage, some blockchains have adopted a different form of consensus, Proof of Stake (PoS). In the PoS model, rather than spending energy to solve a cryptographic puzzle, nodes called “validators” will lock up a certain amount of tokens to win a chance at proposing and validating new blocks.

So in PoW, the higher your hashrate (a measure of computing power), the higher your likelihood of being able to mine a new block. In PoS, the more of the native token you have staked, the higher your likelihood of being able to mine a new block. Validators are rewarded for honest behavior (proposing and validating legitimate transactions) and punished for dishonest behavior (attempting to write fraudulent blocks to the chain) by having their staked tokens slashed or burned.

The majority of blockchains today utilize some form of PoS as their consensus mechanisms, although with many different implementations. Some of the most popular include Ethereum, Solana, Avalanche, Cosmos, and NEAR.

### Emerging Consensus Mechanisms
#### Proof of Transfer
Proof of Transfer (PoX) is a consensus mechanism unique to the Stacks blockchain.

![image](https://user-images.githubusercontent.com/110959584/193432795-89406753-2b03-4cb3-b0b7-8cac129b9f6e.png)

Stacks is a Layer 1 blockchain that allows for smart contracts and dapps to be built, and ultimately settle, on Bitcoin. Bitcoin itself cannot run smart contracts. This is by design, as the goal behind Bitcoin is to keep the foundational layer as simple as possible. Through Proof of Transfer, Stacks seeks to expand Bitcoin’s functionality by allowing smart contracts without changing anything about Bitcoin itself.

Proof of Transfer works similarly to Proof of Work. You can think of PoX as a secondary layer to PoW. Where in PoW, Bitcoin miners commit energy for a chance at mining a block, in PoX, Stacks miners commit Bitcoin for a chance at mining a block. Because of this unique model, Stacks can recycle the energy used to mine Bitcoin and utilize it to unlock Bitcoin’s potential as a productive asset.

#### Proof of Burn
Proof of Burn is similar to Proof of Transfer, except the asset being transferred is destroyed. The economic model here is similar in that miners are spending one external resource to gain another. The primary difference is that the value is destroyed and not transferred anywhere.

#### Proof of History
Proof of History is a unique consensus mechanism utilized by Solana, along with Proof of Stake. Proof of History is a mechanism that allows validator nodes to quickly verify that a certain transaction happened between two specific points in time in the blockchain.

This is part of what gives Solana its speed! It allows for fast verification that a certain amount of time has passed between two blocks, and it also allows for horizontal scaling because mutiple pieces of the chain can be verified at any given time.

#### Proof of Space
Proof of Space is another consensus mechanism used by the Chia decentralized storage network. Proof of Space is a method for users to prove they are keeping unused space on a hard drive in reserve for network storage. A cryptographic collection of numbers is stored on a user’s disk and these represent plots: a special unit of storage. The users with the largest number of plots available have the highest chance of winning the next block.

#### Proof of Access
The Arweave protocol utilizes an interesting consensus mechanism called Proof of Access. To understand Proof of Access, it’s helpful to understand that Arweave is a blockweave, rather than a blockchain. While a blockchain is a collection of blocks where each block is linked to the previous block, a blockweave is a collection of blocks where each block is linked to multiple previous blocks.

The purpose of Arweave is decentralized, permanent storage, so Proof of Access is designed to incentive miners to make certain blocks available. Miners are encouraged to replicate valuable data on the network and make that data accessible, resulting in AR token rewards.
