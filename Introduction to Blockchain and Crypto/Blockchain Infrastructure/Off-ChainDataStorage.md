# Off-Chain Data Storage
Not all data should be stored on-chain! This is a topic of endless debate and discussion, but blockchains have a very specific use case and are meant to be permanent,
historical ledgers of transactions. Because of their distributed nature, it is expensive to store data on a blockchain. They are not meant to replace traditional
database storage.

This is an important topic in web3 development, so let’s look at the use cases of web3 development. The goal is to provide software that is distributed, immutable,
and censorship/tamper-resistant. It’s important to remember that every state change that is written to the blockchain has to be paid for. It’s a common misconception
that all of our data needs to be stored on-chain in order for it to be trustless and immutable, but this is not the case. It’s important to carefully consider the
amount and type of data we want to store on-chain and look at the most effective way to do so, even if it takes a little more effort and clever engineering.

Let’s look at our fictional app here. One potential set of data we might have is product information. For each product, we might need to store the:

- ```name```
- ```description```
- ```price```
- ```image```

Do we want to store all that in a smart contract where every byte of data is paid for by the user? Definitely not. That would get very expensive very quickly!
What happens if we want to modify our data structure? We would have to perform a complex contract migration just to add a simple field like a product_id.

This is where some of the misconceptions around of web3 come in - people imagine a decentralized Twitter where they have to pay a transaction fee and wait forever
anytime they post or respond to a tweet, but this is not a pragmatic approach to web3 development!

What should we do instead? What we really care about here is trustless data integrity. We want to ensure that our data can’t be tampered with and that it is
transparently verifiable. What we could instead do is store the data off-chain in either a traditional database or in a decentralized solution.
Then, we store a hash of that data on-chain in our smart contract. This way we are guaranteeing the validity of our data on-chain without having to store
the data itself. Then, in our app, we compare the hash with the hash stored on-chain to verify any changes.

We can combine this with a wallet-based authentication method. We submit a transaction, containing our address and data hash, to our smart contract, then another
part of our app submits the actual data change to our database simultaneously. Because our authenticated address is the only one that could have authorized the
transaction on-chain, we can know whether or not our data was tampered with. By utilizing a decentralized data storage solution like Gun, we get the best of both
worlds and get decentralized data storage without the expensive inefficiencies of writing that data to the chain.

Some options for this are:

- Gun
- Arweave
- IPFS
- Gaia
- Ceramic Network
