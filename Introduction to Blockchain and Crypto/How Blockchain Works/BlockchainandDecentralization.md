# Blockchain and Decentralization

## Learning Objectives
This article is meant to be a high-level introduction to the big picture of web3 and decentralization. Let’s dive into decentralization:

* What decentralization means
* Why decentralization is useful
* How blockchains accomplish decentralization

## What Does Decentralization Mean?
The simplest way to think about decentralized versus traditional centralized software is that centralized software is hosted and runs on a single computer or multiple computers run by a single entity. In a decentralized (or distributed) system, the code is running across a collection of computers all owned by individual entities. This network is usually open for anyone to join and participate in running a node.

A gif showing a block that is waited to be validated by a large network

It’s important to note that decentralized systems are not unique to blockchains. Peer-to-peer (P2P) networks like BitTorrent have existed for years. So what’s the difference?

A P2P network like BitTorrent is a collection of different people running file hosting servers. With this model, if we want to download a file, we can download it from any of the servers in the network that host it, rather than needing to rely on a single source to download it.

Two other P2P networks with different use cases are:

Gun (a P2P database): Gun works similarly to BitTorrent, except it is used as traditional CRUD data storage that is hosted collectively across the network.
Lightning (a P2P payment network for Bitcoin): Lightning is a P2P layer 2 for Bitcoin. Lightning allows users to scale Bitcoin transactions by keeping a channel open, recording all the different transactions until the channel is closed, and sending the entire record of transactions to the Bitcoin chain at once.
There is one key difference between a blockchain like Bitcoin and a P2P network like Lightning or Gun. P2P networks are ephemeral and don’t have a global state record, whereas blockchains do.

## Why is Decentralization Useful?
There are three key benefits of decentralization:

Security: The “crypto” in cryptocurrency comes from cryptography. This is the mechanism that secures individual transactions on the blockchain as well as provides the backbone of the consensus mechanism known as Proof of Work. By leveraging public key cryptography, we can create highly secure identity and user management, despite the information and transactions being public.
Transparency: Because blockchain networks are (or should be) open and viewable to all, they are highly transparent. If the network is not open and nodes are not able to be downloaded and verified by anybody, we cannot call the network decentralized.
Permanence: Because of the ledger-like nature of blockchain networks, information written to blockchains is permanent. A blockchain is literally a chain of data blocks that are all connected together, so every transaction is recorded to that ledger permanently.
This trifecta of security, transparency, and permanence is what makes blockchain technology the ideal solution to create important infrastructure like money! It is also what allows us to use them to create censorship-resistant software that is not controlled by any one entity. This enables us to create technology and software that is open and accessible to all and cannot be blocked or censored. This is what we’ll be exploring for the remainder of this course.

## How do Blockchains Accomplish Decentralization?
The best way to think about a blockchain is to imagine it like a ledger. At its core, that’s what a blockchain is: a globally verifiable ledger of transactions that is collectively run and verified by each member of the network. It is a ledger of transactions that every user has access to.

Imagine if Hogwarts had a “magical” accounting ledger that recorded every transaction that occurred at the school. Rather than being a traditional ledger where someone would write down the transaction in a single book, and everyone had to trust the transaction wasn’t fabricated, this book has special properties. Anybody interested can obtain their own copy of this book, and anytime anybody makes a transaction, the ledger updates everyone at the same time.

A gif showing a that all of the computers in the network have a record of the transaction.

The key innovation of blockchains is solving the Byzantine Generals problem. Digital currencies had been in the works for years, but the core problem that nobody had cracked yet was the Byzantine Generals problem, also known as the double spending problem. The groundbreaking work of solving this problem was done by Satoshi Nakamoto when they created Bitcoin.

Bitcoin and the double spending problem
The double spending problem is essentially the difficulty of preventing the duplication of digital content. Going back to our P2P network example, like BitTorrent, double spending is not a problem. In an architecture like this, duplication of data is not only okay, but an expected part of the design, as we want data hosted by multiple people so it can be downloaded from multiple sources.

With a blockchain, however, we don’t want transactions to be duplicated.

An image showing that Bitcoin doesn't allow for transactions to be duplicated.

If we are using the use case of money, the original and one of the primary use cases for blockchain technology, a user being able to create a transaction where they send money to one person and then duplicate that transaction and send the money to someone else is unacceptable! This is the roadblock previous attempts at digital currency had run into and is essentially the reason why centralized institutions like banks exist. Before Bitcoin, a trusted third party was required to verify transactions to prevent this.

So how can we solve this problem without a centralized authority? This is where the distributed ledger comes into play. At a high level, it makes it so that any transaction is required to be recorded to the entire network so it can’t be duplicated. In the case of Bitcoin, a user’s currency is moved from their wallet (the record of how much of a token they currently own) to someone else’s wallet. This process is recorded to and verified by the entire network simultaneously, so it can’t happen twice.

Although money is the primary use case, it has implications for other technologies as well, which we’ll cover throughout this course. But all of them stem from this basic problem and solution of being able to verify the authenticity of some code across an entire network.

Let’s dive in and explore the world of crypto and web3 so you can get your career off on the right foot!
