# Creating a Metaverse and a Web3 Stack
In this article, learn what a metaverse means when we’re talking about Blockchain.

## What is the Metaverse?
The Metaverse is one of those terms that is hard to define. For our purposes we can define it as a cohesive collection of web3 tech that allows people to work
toward an overarching goal. It doesn’t necessarily have to imply any sort of gaming or virtual reality. All it really is is a set of connected web3
protocols all centered around a common goal.

By creating a metaverse, we can create an entire ecosystem not limited by physical boundaries, where each component is transparent and verifiable on-chain.
This opens up a world of possibilities for people to collaborate with each other and create value for the world.

Our task is to model out how we would lay out our entire tech stack, smart contracts included, to create a metaverse of sorts where each component of our dapp
interacts with another to create a cohesive ecosystem.

## The Cheddarverse
Let’s look at the example of our Cheddar app.

![image](https://user-images.githubusercontent.com/110959584/199620145-89af4643-927b-4f87-b287-7200df340808.png)

An image showing the Cheddar app. Items on it look like they're made out of cheese and sell for different amount of coins.

Let’s say we’ve decided on using Stacks. We want our dapp to be completely decentralized, with no centralized components, so here’s how we might structure our tech
stack based on the components we have discussed so far.

### Blockchain
We’ll be using the Stacks blockchain to build out Cheddar.

### Indexing & Querying
Since we want it to be as decentralized as possible, we’ll go with the KYVE Network, which has an integration with Stacks in order to index and query data.

### Blockchain API
In order to actually interact with and send transactions to the blockchain, we’ll utilize the Stacks API. This is not as decentralized as we would like,
but it’s the best option for our particular application.

### Oracle
We may need an oracle in order to pull in asset prices. In this case, we can use Redstone, as it has a Stacks integration.

### Development Environment
Since we’re using Stacks, we’ll use Clarinet as our development environment to get our mock network running.

### Wallet & Identity Management
The most popular wallet in the Stacks ecosystem for interacting with dapps is the Hiro Web Wallet, so we’ll use that.

### Off-Chain Storage
For hosting files permanently, we can utilize Arweave, which we can also utilize to host our front end. For database storage, which doesn’t need to be on-chain,
we can integrate with Gun.

### Frontend
Finally, we can use the lightweight micro-stacks library to connect our client to the blockchain.

### Smart Contracts
Now we need to map out how we want my smart contracts to interact.

- We want to create a CheddarCreator NFT collection that serves as a utility token to become a creator on Cheddar and to become a member of CheddarDAO.
- As a member of CheddarDAO, we can vote on proposals that will dictate where the future of the platform is headed.
- Our web app UI should be able to check for both our NFT and DAO membership in order for us to take certain actions.

We can start to see how this all weaves together to create a decentralized ecosystem based around a shared goal!
