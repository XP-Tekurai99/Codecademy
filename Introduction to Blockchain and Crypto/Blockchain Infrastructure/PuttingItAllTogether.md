# Putting It All Together
With all that in mind, let’s look at how we might build our fictional app using this stack.

- First, we need to choose what chain we want to build on. Let’s say we choose to build on Stacks.
- The next thing we would need to do is decide how we want to access the data from the blockchain. In this case, we’ll utilize the Stacks API provided by Hiro.
- Next we’ll get set up with our Clarinet development environment so we can spin up a local chain.
- And we’ll need to integrate our app with the Hiro Web Wallet for authentication and identity management.
- We’ll also have some data that we don’t necessarily want on-chain, so we’ll set ourselves up with Gun.eco for our decentralized off-chain data storage.
- Next we need to choose a client library, and in this case we’ll choose Micro-Stacks and build our actual front end using Remix.
- Finally, we need a way to host our dapp. We can go the traditional route of centralized hosting using something like Vercel or Netlify.
Or, if we want our dapp, to be 100% decentralized we can deploy it to Arweave or IPFS.

This process is still relatively involved, and this is the basic process you’ll go through each time you want to build a new dapp.
You’ll need to consider which pieces you want decentralized and which you want centralized, what should be on-chain and off-chain, and what the
right tool for each job is. As you continue to explore the web3 ecosystem and practice building more dapps, you’ll start to both discover new tools and learn
which are best for which task.
