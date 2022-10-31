# Smart Contract Languages: Solidity, Clarity, and Rust
In this article, we’ll look at Solidity, Clarity, and Rust.

## Smart Contract Languages
Now that we’ve looked at the conceptual ideas and applications behind smart contracts, let’s get a bit more technical and look at how we can actually build them. There are many different smart contract languages, just as there are many different chains. We’ll be looking at three of them:

- Solidity
- Clarity
- Rust

### Solidity
Solidity is the smart contract language used on the Ethereum chain, as well as most other EVM chains like Polygon and Avalanche. Solidity is the first and most commonly used smart contracting language, and currently dominates the market of developers. If you are used to writing JavaScript, Solidity will likely feel relatively familiar, as it shares a lot of the same properties and structure.

An example of Solidity code from the ethereum GitHub repo.

```
// SPDX-License-Identifier: MIT
pragma solidity >=0.6.0 <0.9.0;
 
contract HelloWorld {
    function helloWorld() external pure returns (string memory) {
        return "Hello, World!";
    }
}
```

However, over the years Solidity has come under scrutiny and been partially to blame for a lot of the high-profile attacks on projects in the Ethereum space. Solidity is object-oriented and Turing complete. These two properties, while useful, can be dangerous when writing smart contracts. The object-oriented nature of Solidity means that much of the code you write may have implicit functionality from an inherited class that may not be obvious as the developer. Furthermore, the Turing completeness and resulting Turing complexity introduce problems like difficulty analyzing what a program will do and how much it will cost. It also allows for infinite loops and recursion, which can lead to things like a re-entrancy attack.

While these features are necessary in some languages and use cases, they are arguably a negative in smart contract development, where the code lives on a public chain and writing bad code could potentially negatively impact the entire network. While Solidity is still the clear market leader, developers and chains are beginning to adopt other languages to write smart contracts with.

### Clarity
Clarity is a relatively new smart contract programming language that was built for the Stacks blockchain.

An image of the Stacks Foundation logo.

It was intentionally designed to a language that is safe, secure, and easy for developers to write safe, clear code with. Transparency and explicit code is a must in smart contracts, because peoples’ assets are being handled. Clarity provides unique features that make it an ideal choice for developers who favor security and want a language explicitly designed for safe smart contract programming.

An example of Clarity code from the Hello World tutorial in their GitHub repo:

```
import { Client, Provider, ProviderRegistry, Result } from "@blockstack/clarity";
 
let helloWorldClient: Client;
let provider: Provider;
 
(...)
 
provider = await ProviderRegistry.createProvider();
helloWorldClient = new Client("SP3GWX3NE58KXHESRYE4DYQ1S31PQJTCRXB3PE9SB.hello-world", "hello-world", provider);
 
await helloWorldClient.checkContract();
 
await helloWorldClient.deployContract();
 
const query = helloWorldClient.createQuery({ function: { name: "say-hi", args: [] } });
const receipt = await helloWorldClient.submitQuery(query);
const result = Result.unwrapString(receipt);
```

#### Clarity vs Solidity
If we compare Clarity to Solidity, Clarity differs on a few key fronts. First, it is decideable and intentionally Turing incomplete. This means that you can statically analyze exactly what a function call will do from the code alone, eliminating potential vulnerabilities caused by gas estimation issues and the uncertainty of Solidity code. There is a tradeoff to this - because of the Turing incompleteness, Clarity doesn’t allow looping. This is by design, as we avoid the trap of infinite loops and recursion. This prevents issues like the halting problem. This refers to a potentially never-ending program which is a huge issue and potential source of DDoS on a distributed network.

Clarity also avoids re-entrancy. Re-entrancy is not allowed with Clarity. Instead of looping, we can iterate through data structures in Clarity.

Clarity is also not object-oriented. This results in more explicit, verbose code, rather than implicit functionality that is not clear to either developers or smart contract auditors.

### Rust
Chains like Solana and NEAR utilize Rust to build their smart contracts. Rust is a very popular language that actually has the highest developer satisfaction of any language.

An example of “Hello World!” in Rust:

```
fn main() {
    println!("Hello World!");
}
```

Rust is growing in popularity due to multiple factors like its robust tooling ecosystem, the fact that it is type safe and memory safe, generates small binaries, and has some advanced optimizations that can remove dead code.
