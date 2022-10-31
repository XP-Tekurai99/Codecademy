# Blockchain and Web2 vs Web3 Architecture
In this article, learn about Decentralized Apps (Dapps) and the difference between web2 and web3.

## Decentralized Apps (Dapps)
Web2 vs Web3 Applications
What is a dapp?
A Decentralized Application (Dapp) is essentially an application that has at least one component hosted on a decentralized architecture.
Dapps exist on a spectrum. We can have dapps where there is some core functionality that runs on a blockchain via a smart contract,
but everything else runs on traditional centralized web2 architecture. Or we can have every single piece of the application running on
some sort of decentralized system.

At an introductory level, we can define web3 and web2 as:

Web2: Web applications that are built on architecture that is owned and controlled by a single entity.

Web3: Web applications that are built on architecture that is distributed among a decentralized network of entities.

At the heart of web3 development is the concept of recreating web2 web applications on top of decentralized blockchain architecture.

## Web2 vs Web3 stacks
A typical, simplified web2 stack might include a:

- Client
- Server
- Database

The client and server may be hosted on the same server, or they may be hosted on different servers. The database will typically be hosted
along with the server, although it can be hosted elsewhere.

Let’s look at a hypothetical web2 app and see how we might recreate it under a web3 architecture. Let’s imagine a fictional app called Cheddar.

Cheddar is an app used to buy and sell digital products. It’s for independent creators to upload their products and easily sell them to anybody who wants to buy them.

Let’s look at what we might use for a tech stack to build this out.

- Front End: Next.js
- API/Authentication/Database/File Storage: Supabase
- Hosting: Vercel
- Payments: Stripe

This hypothetical tech stack represents what we might need to build out this application on a traditional web2 architecture. It’s important to note there’s
nothing wrong with building something out this way! Centralized apps aren’t going anywhere and are still useful and should be used instead of decentralized
architectures in many cases.

For example, an internal warehouse management software for a local office supply company that relies on real-time updates would not really benefit from being
on a globally distributed network.

But let’s say our hypothetical company, Cheddar, is focused on allowing people worldwide to gain financial independence by creating and selling their own
digital creations like art, music, and writing. In this case, if Cheddar was based in the US, there are likely millions of people across the world that
will never be able to benefit from our app because of government restrictions that prevent them from using it or making money from it.

We could benefit from building our app on globally accessible and censorship-resistant architecture. If we were going to recreate this same web2 app
utilizing decentralized architecture, our stack would look different.

In web3, each of the web2 components has a corresponding component in web3, although they function and interact a bit differently.
Here’s how the architecture components from above might translate into a decentralized version.

- Front End: Next.js (stays the same)
- API: Data from smart contracts and the blockchain itself
- Authentication: Decentralized identity management via wallet software like Metamask, Hiro, or Phantom
- Database: Combination of storing data directly in smart contracts and using decentralized data storage
- File Storage: Decentralized data storage system like IPFS, Arweave, or Gun
- Hosting: Similar to file storage mechanisms like IPFS or Arweave
- Payments: Direct payments on-chain using the corresponding cryptocurrency

![image](https://user-images.githubusercontent.com/110959584/198913844-ea80c170-bdec-4e03-9965-8dd40339e3f9.png)

It’s also important to note that we can implement a combination of these methods and architecture decisions. For example, I could have a web app that utilizes
smart contracts on a blockchain, but the front end code, off-chain data, and assets are all stored on traditional web2 architecture. It all comes
down to your specific use case and how much you want to be truly decentralized.
