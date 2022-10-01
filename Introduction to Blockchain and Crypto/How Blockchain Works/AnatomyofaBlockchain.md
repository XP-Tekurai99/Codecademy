# Anatomy of a Blockchain
![image](https://user-images.githubusercontent.com/110959584/193426506-590f71d1-2de9-44eb-bfff-eb32bf9aa304.png)

## Learning Objectives
By understanding how blockchains work and the technical problems they solve, you’ll be better positioned to make the most informed choice for what chain you’d like to explore building on for your personal crypto journey.

A proper understanding of the fundamentals will help you spot projects that are likely to be around for the long term vs projects that are just trying to jump on the bandwagon.

## Anatomy
Every blockchain network handles things slightly differently, so this process will vary depending on what network you are working with (particularly when we look at Proof of Work vs Proof of Stake) but they all share some similar characteristics. The mechanism we’ll be looking at is a simplified view of how Proof of Work blockchains function. There are three main components of a blockchain design that underpin its functionality:

* Blocks
* Nodes
* Miners

An image that shows a miners mines a block, which is made up of a data, a nonce, and a hash, and then that block is sent to nodes.

### Blocks
The blocks are the chunks of data that make up the blockchain. You can think of a blockchain as a chain of blocks of data connected to each other via their timestamps and hashes of their data.

Every block has three basic elements:

Data: The data contained in and written to the block.
Nonce: The nonce is a randomly generated 32-bit whole number that generates a block header hash.
Hash: The hash is a 256-bit number that is connected to the nonce.
When the first block in a chain is created, a nonce generates the cryptographic hash.

### Nodes
This chain of blocks is useless unless this ledger and process of writing new blocks can be watched and verified by a large number of distributed computers. These computers are called nodes. In an open network, like Bitcoin, anybody can connect to the network and run a node. These nodes are responsible for independently approving each new block that gets mined. The entire network of nodes must approve a block for it to be successfully mined.

This decentralization of nodes is what makes a blockchain decentralized. Unfortunately, decentralization and scaling a blockchain always comes with trade-offs: The greater the computing requirements of a blockchain node, the less decentralized it can be. To scale a blockchain and increase transaction throughput, we will usually need to discuss decreasing the number of nodes on the network required to approve the transaction.

Note: Nodes are only responsible for holding a copy of the existing blockchain, not adding new blocks. That role falls to miners.

### Miners
So, how does mining work? Miners are in charge of creating new blocks on the blockchain. Every block has its own nonce and hash, but every block also references the previous block’s hash. In a Proof of Work system, mining is the process of utilizing software to brute force guess the correct nonce that will generate the correct hash. A miner needs to go through roughly 4 billion permutations until the correct nonce is found. Finding the correct nonce is the “proof of work” that the consensus mechanism is named after.

A gif showing how Proof of Work works. It takes a hash, adds difference nonces to it, calculates the SHA-256 hash, and keeps doing this until a valid hash is found.

When miners submit a nonce, it gets run through a cryptography function that will output a hash. Only when a miner gets the hash correct do they get to mine the next block.

## How Bitcoin Solves the Double Spending Problem
What’s the purpose of the brute-force guessing process?

The computational work (and energy expenditure) required to mine a new block is key to understanding how Bitcoin solves the double spending problem. (Remember that a node is a computer that hosts a copy of the blockchain.)

What would happen if one of these nodes tried to broadcast a fake transaction?

An example: using the same Bitcoin twice
Let’s say that we tried to use our Bitcoin to buy an online course, and then immediately tried to use that same Bitcoin to order food. How does the network know which transaction to process?

Note: When a Bitcoin transaction occurs, it is passed one by one through each node on the network, so not every node gets notified at the same time.

Bitcoin without proof of work
If the process for adding new blocks was free, any node, and any Bitcoin user, could add whatever transaction they want, and the rest of the network would have no way of knowing if they should include that transaction in their copy of the ledger or not.

The network would be in disagreement about whether the online course or the food transaction should be included in the ledger.

Bitcoin with proof of work
To solve the problem that free blocks would create, we can return to our Proof of Work consensus mechanism: The node that solves the puzzle gets to be the one to write the new data, and the competing transaction would be dropped.

Because there are also multiple miners on the network, in order to successfully create a fake transaction, we would have to control the mining power of 51% of the network, which is an enormous resource expenditure.

This is where a lot of the security of a blockchain comes in! To change a block in the chain, an attacker would also need to re-mine every single block that comes after. This can seem an almost impossible task.

Once the correct nonce is found and the hash matched, the miner writes the block, its data, and its header hash to the chain, and the change is accepted by all the nodes in the network.
