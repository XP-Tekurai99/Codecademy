# Smart Contracts
In this article, we’re going to get into the essential building blocks of the programmable blockchain: smart contracts.

## What we’ll be learning
The landscape of smart contracts is large, and there are multiple languages to write them in, just as there are multiple chains to build on. We’ll give a high-level overview of what smart contracts are and what they’re used for.

## What are Smart Contracts?
At their core, smart contracts are chunks of code that live on the blockchain. If we think of a backend server with code running on it, smart contracts are very similar. The main difference is that smart contracts are publicly accessible and immutable.

### Publicly Accessible and Transparent
Since the blockchain is a shared historical ledger, all nodes have access to it, which means it is open and accessible to anybody. When we write a smart contract and deploy it to a blockchain, we are initiating a transaction to write that data to the blockchain. Then anybody can call that smart contract and interact with it.

So how do we secure smart contracts? That’s up to the developer. Smart contract languages like Solidity and Clarity have access control functionality built-in, so we can restrict function calls to certain addresses.

Note: This is a theme in decentralized software - rather than having functionality or data hidden behind a server, it is publicly viewable by anyone, but uses cryptography to determine who has access to modify or view certain pieces.

### Immutable
Smart contracts are also (partially) immutable. Once a smart contract is deployed, the foundational code can’t be changed. We can modify the data only by calling functions defined in the smart contract.

In something like a JavaScript program, if we modify data, we need to save it to a database for it to persist. In a smart contract, if data is modified, it gets modified by the user sending a transaction and that change is permanently written to the blockchain. Rather than storing the data in a database, the change happens directly in the code itself on-chain. This process is inefficient and should only be used for the critical data that needs to be stored on-chain.

Transparency and immutability are what give smart contracts their superpowers. These traits allow us to use smart contracts to build decentralized financial systems that are:

## Accessible to Everyone
Censorship-resistant web applications
Permanent verifiable records of ownership (via NFTs)
Transparent organizations via (DAOs)
Let’s dive into what smart contracts are used for and some common pitfalls to avoid.

## What are smart contracts used for?
Smart contracts should be used for any functionality that needs to be trustless. Essentially, any use case where having a singular, central intermediary could result in corruption of data or functionality, could benefit from a smart contract. Some of the most common use cases are:

Finance
Gaming
Legal
Real estate
Corporate structures
### Finance and DeFi
One of the most common use cases for smart contracts is in the world of finance. This makes sense, as the original use for blockchain technology itself was Bitcoin, designed to be a superior form of money. You can think of financial smart contracts, also known as Decentralized Finance (DeFi), as replacing any functionality of a bank. This has profound implications for the world and the economy. What Bitcoin did for money, DeFi has the potential to do for the economy.

A limitation of Bitcoin is that it cannot be productive without modifying its core functionality, which introduces additional attack vectors. Ethereum was created in order to create a network that is able to be programmable money. This made it possible to not only create a form of money based on immutable code, but to recreate financial services using immutable, transparent code.

While Ethereum takes the approach of having the money and robust programmability on the same layer, other chains like Stacks separate these two layers. Stacks uses Bitcoin as the underlying money and settlement layer, while the Stacks chain handles the programmability. This architecture allows us to keep the money layer simple while still having robust smart contract functionality with Bitcoin. Imagine recreating a small business loan or a mortgage, but instead of having to trust a bank, the entire thing is handled by smart contract code.

### DeFi problems
DeFi is not without its share of problems. Having a decentralized collection of smart contracts handle our assets means:

It is up to the developers to write secure code
There is no central intermediary to save us if something goes wrong.
We have all heard of the numerous hacks and collapses that have occurred on DeFi protocols, and we have seen the collapse of entities like Luna and Celsius.

This should serve as a warning for those who see the potential of web3 to transform the financial sector. We are still early in this industry, and we
need to pay close attention to how we build these protocols. DeFi has the potential to unlock financial tools for people who can’t access the modern
financial system most of us take for granted.

### Gaming
While DeFi is one of the most promising and popular uses of smart contracts right now, NFTs are also growing in popularity and are beginning to show
some promising use cases. Most of us are familiar with the idea of profile picture NFTs, those collections of cartoon
avatars that can sell for millions of dollars.

![image](https://user-images.githubusercontent.com/110959584/196067518-cc1af229-9db7-4dfe-992c-cb6a76b0f627.png)

A rendering of the "bored ape" NFT.

But this is only one, and likely introductory, use of NFTs. Another area NFTs are being put to use is in gaming.

As an example, let’s take a game like World of Warcraft. People spend thousands of dollars in real-world money to collect rare items in games like this. But their ownership of that item is fragile and dependent on the company. Technically, the company owns the digital item. With NFTs, gamers can have an immutable and verifiable record of ownership of their in-game assets.

### Legal
One of the most interesting potential use cases for smart contracts is legal agreements. There is a saying in the blockchain world: “Code is law.” This means that whatever the code says, goes. If we apply this to legal agreements, we may see a future where people sign transactions using their wallets and commit to taking a certain action on-chain. We are already starting to see this! Arizona currently allows enforceable legal agreements to be issued via blockchain, and California allows marriage licenses to do the same.

Many people will interject here and say this is a solved problem, but this misses the forest for the trees. Just because we currently have ways of signing legal agreements and documents doesn’t mean that process can’t be improved!

Remember, the underlying goal of blockchain technology is to make information publicly accessible, verifiable, and immutable. Imagine if legal agreements had this level of certainty. It could eliminate many disputes and lawsuits as the record would be verified on-chain for the world to see, rather than being managed by a single entity.

### Real Estate
Real estate is one of the most complex industries with many moving parts and potential for corruption or error. This makes it a great option to be disrupted with some smart contracts. Many of the little hidden costs associated with a new home purchase or build could be drastically reduced or even eliminated if the process was handled by a series of related smart contracts.

Imagine the entire process, from the building agreement, to the mortgage process, to the title, to the municipal record keeping and inspections, all the way to the tokenized registration of ownership via an NFT, being handled with well-audited smart contracts. This would help to eliminate errors in the process, as well as eliminate corruption from any of these parties during the process.

### Potential
Some other industries where people are beginning to explore the potential of blockchain technology are healthcare, logistics and supply chains, IoT, and corporate structures. Any time you encounter a process that suffers from unnecessary middlemen, lack of trust, or loss of data, there is potentially a portion of it that could be improved with blockchain technology.

## Common Smart Contract Exploits and Pitfalls
It’s no secret that writing smart contracts can be dangerous business if done incorrectly. Poorly written smart contracts have been the source of millions of dollars lost or stolen assets. It’s important to be aware of security best practices when writing smart contracts. Some of these will be dependent on the language you are using, but we’ll two common issues here.

For more on this, check out the Decentralized Application Security Project.

### Reentrancy
This is one of the most well-known and infamous smart contract vulnerabilities. It occurs when external contract calls are allowed to make calls to the caller contract before execution finishes. This attack most notably caused The Decentralized Autonomous Organization (DAO) hack, an attack in which the hacker was able to call a function to allocate funds to a newly created DAO over and over again before the ledger of token ownership was updated.

This vulnerability is particularly sinister because it is difficult to spot in audits. It requires looking deeply at the call structure of sets of multiple contracts and functions. Solidity now has a reentrancy guard that can be added. Clarity does not allow reentrancy at all.

### Access Control
Remember, in smart contracts all code is publicly accessible and callable. It is up to the developer to ensure that only the expected, authorized users are able to call in to the relevant functions.

There are others, but these are two of the most common exploits you’ll run into when developing smart contracts, at least with Solidity.
