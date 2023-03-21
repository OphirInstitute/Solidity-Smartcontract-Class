
# Ophir Solidity-Smartcontract-Class

Welcome to the repository for the Ophir Solidity-Smartcontract-Class - Beginner to Expert Full Course | by Ophir!

Recommended Testnet: Sepolia

*We have create the repos to work with Sepolia due to Rinkeby and Kovan being sunset, and Goerli being a disaster. Let us know if yo have any issues!*

# [Testnet Faucets](https://faucets.chain.link)
Main Faucet:<a href="https://faucets.chain.link" target="_blank"> https://faucets.chain.link</a>
Backup Faucet:<a href="https://sepoliafaucet.com/" target="_blank"> https://sepoliafaucet.com/</a>

> ⚠️ All code associated with this course is for demo purposes only. They have not been audited and should not be considered production ready. Please use at your own risk. 

# Resources For This Course

### Questions

-   [Chat GPT](https://chat.openai.com/chat)
    -   Ask questions and chat about the course here!
-   [Stack Exchange Ethereum](https://ethereum.stackexchange.com/)
    -   Great place for asking technical questions about Ethereum
-   [StackOverflow](https://stackoverflow.com/)
    -   Great place for asking technical questions overall


# Table of Contents

<details>
<summary>Resources</summary>
<ol>
<li><a href="#testnet-faucets">Testnet Faucets</a></li>
<li><a href="#resources-for-this-course">Resources For This Course</a><ul>
<li><a href="#questions">Questions</a></li>
</ul>
</li>
<li><a href="#table-of-contents">Table of Contents</a></li>
</ol>
</details>

<details>
<summary> <a href="#Module-1-Introduction-to-Solidity-and-the-Ethereum-Network">Module 1: Introduction to Solidity and the Ethereum Network</a></summary>
<ol>
  <li>
  <a href="#Overview-of-Solidity-programming-language">Overview of Solidity programming language! </a>
  </li>
  <li>
  <a href="#Introduction-to-the-Ethereum-network">Introduction to the Ethereum network </a>
  </li>
  <li>
  <a href="#Understanding-of-blockchain-and-smart-contracts">Understanding of blockchain and smart contracts </a>
  </li>
</ol>
  
</details>
<details>
<summary> <a href="#Module-2-Creating-Your-Own-Token"> Module-2-Creating-Your-Own-Token </a> </summary>
<ol>
<li>
<a href="#Defining a token contract">What is a Blockchain? What does a blockchain do?</a>
</li>
<li><a href="#Adding-functions-for-transferring-and-tracking-token-balance">Adding functions for transferring and tracking token balance</a></li>
<li><a href="#Implementing-the-ERC-20-standard-for-interoperability">Implementing the ERC-20 standard for interoperability</a></li>
<li><a href="#Deploying-your-token-contract">Deploying your token contract</a></li>
</ol>
</details>
<details>
<summary><a href="#Module-3-Creating-Your-Own-NFT">Module 3: Creating Your Own NFT</a></summary>
<ol>
<li><a href="#Defining-a-token-contract">Defining a token contract</a></li>
<li><a href="#Adding-unique-identifier,-metadata,-and-ownership-information">Adding unique identifier, metadata, and ownership information</a></li>
<li><a href="#Adding-functions-for-transferring-and-tracking-NFT-ownership">Adding functions for transferring and tracking NFT ownership</a></li>
<li><a href="#Implementing-the-ERC-721-standard-for-interoperability">Implementing the ERC-721 standard for interoperability</a></li>
<li><a href="#Testing-and-deploying-your-NFT-contract">Testing and deploying your NFT contract</a></li>
</ol>
</details>
<details>
<summary><a href="#Module-4-Advanced-Concepts-in-Token-and-NFT-Creation">Module 4: Advanced Concepts in Token and NFT Creation</a></summary>
<ol>
<li><a href="#Adding-additional-features-to-your-token-and-NFT-contracts">Adding additional features to your token and NFT contracts</a></li>
<li><a href="#Understanding-token-economics-and-designing-incentives">Understanding token economics and designing incentives</a></li>
<li><a href="#Creating-a-user-interface-for-your-token-and-NFT">Creating a user interface for your token and NFT</a></li>
<li><a href="#Security-best-practices-for-smart-contract-development">Security best practices for smart contract development</a></li>
</ol>
</details>


# Module 1: Introduction to Solidity and Ethereum Network

## Overview of solidity programming language
Introduction to Solidity

### - What is Solidity?

- 8yrs Ago, precisely, August 2014, @gavofyork submitted a proposal to develop a language that would transform the #Ethereum ecosystem, implementing amazing “programs” that will be so effective in “blockchain interactions”.

These “programs” are “smart contracts”
They allow humans to interact with the blockchain
(more on this later)

- Other developers such as @ethchris, @alexberegszaszi and several other developers with @ethchris as team lead helped develop this language and called it solidity.

- Solidity is an object Oriented programming language influenced by c++ , JavaScript and Python.

It implements Smart-contracts on various blockchain platforms especially #Ethereum.

- Object-Oriented languages are languages that have foundation in the use of objects.
- Objects are the basic units of the language
- They are used to form classes which are in turn used to produce applications.

- A brief dive into solidity Syntax

In computer programming, syntax refers to the set of rules that govern the structure and arrangement of code in a particular programming language. It specifies how statements, expressions, and other programming constructs should be written in order to be considered valid and meaningful by the computer.

In solidity the syntax simply refers to the way solidity codes are written.

Solidity is similar to JavaScript and C++

It is not possible to list all of the Solidity syntax here, as it is a comprehensive programming language with many different features and constructs. However, here is an overview of some of the main syntax elements used in Solidity:

⁃ Comments:

Solidity supports both:

1. single-line comments ``(denoted by "//")``

2. multi-line comments ``(denoted by "/* ... */").``

⁃ Variables:

Solidity supports several data types for variables, including:

Value data types:

### Boolean- bool,

(represents true or false values.)

``pragma solidity ^0.8.0;``

``contract ExampleContract {``
``bool myBool = true;``

``function getBool() public view returns (bool) {``
``return myBool;``
``}``
``}``

*In this example, we define a boolean variable "myBool" and initialize it to true. The "getBool" function returns the value of "myBool".




### Integer- int & Unsigned- uint,

(represents whole numbers, either signed or unsigned.)

`pragma solidity ^0.8.0;`

``contract ExampleContract {``
``int256 myInt = -123;``
``uint256 myUint = 456;``

``function getInt() public view returns (int256) {``
``return myInt;``
``}``

``function getUint() public view returns (uint256) {``
``return myUint;``
``}``
``}``

*In this example, we define an integer variable "myInt" and initialize it to -123, and an unsigned integer variable "myUint" and initialize it to 456. The "getInt" function returns the value of "myInt", and the "getUint" function returns the value of "myUint".

### fixed point numbers - fixed,

(represents decimal numbers with a fixed number of digits.)

``pragma solidity ^0.8.0;``

``1contract ExampleContract {``
``fixed256x18 myFixed = 123.456;``

``function getFixed() public view returns (fixed256x18) {``
``return myFixed;``
``}``
``}``

*In this example, we define a fixed point number variable "myFixed" with 18 decimal places and initialize it to 123.456. The "getFixed" function returns the value of "myFixed".

Address- address,

(represents an Ethereum address.)

``pragma solidity ^0.8.0;``

``contract ExampleContract {``
``address payable myAddress = payable(0x1234567890123456789012345678901234567890);``

``function getAddress() public view returns (address payable) {``
``return myAddress;``
``}``
``}``

*In this example, we define an address variable "myAddress" and initialize it to the Ethereum address "0x1234567890123456789012345678901234567890". The "getAddress" function returns the value of "myAddress".


### bytes,

(represents a single byte of data.)

``pragma solidity ^0.8.0;``

``contract ExampleContract {``
``bytes32 myBytes = hex"00112233445566778899aabbccddeeff";``

``function getBytes() public view returns (bytes32) {``
``return myBytes;``
``}``
``}``

*In this example, we define a bytes variable "myBytes" and initialize it to the hex value "00112233445566778899aabbccddeeff". The "getBytes" function returns the value of "myBytes".



Enums

(represents a set of named constants.)


pragma solidity ^0.8.0;

contract ExampleContract {
enum State { New, InProgress, Completed }
State myState = State.New;

function getState() public view returns (State) {
return myState;
}
}

In this example, we define an enum "State" with three possible values: "New", "InProgress", and "Completed". We also define an enum variable "myState" and initialize it to "New". The "getState" function returns the value of "myState".


Variables can be declared using the syntax "type name = value;".

Reference data types:



Arrays

(Solidity supports both fixed-size and dynamic arrays, which can be of any data type.)

pragma solidity ^0.8.0;

contract ExampleContract {
uint256[] myArray;

function addValue(uint256 newValue) public {
myArray.push(newValue);
}

function getValue(uint256 index) public view returns (uint256) {
return myArray[index];
}
}

In this example, we define an empty dynamic array of uint256 values called "myArray". The "addValue" function allows values to be added to the array, and the "getValue" function allows values to be retrieved from the array using an index value

Structs

(Structs are used to group related data together. They can contain multiple data types, including other structs or arrays.)

pragma solidity ^0.8.0;

contract ExampleContract {
struct Person {
string name;
uint256 age;
}

Person myPerson;

function setPerson(string memory newName, uint256 newAge) public {
myPerson = Person(newName, newAge);
}

function getPerson() public view returns (string memory, uint256) {
return (myPerson.name, myPerson.age);
}
}

In this example, we define a struct "Person" with two fields: "name" and "age". We then define a variable "myPerson" of type "Person". The "setPerson" function allows a new Person object to be created and assigned to "myPerson", and the "getPerson" function returns the values of "myPerson"'s "name" and "age" fields.

Mappings:

(Mappings are used to create key-value pairs, similar to dictionaries or hash tables in other languages. They are particularly useful for creating data lookups.)

pragma solidity ^0.8.0;

contract ExampleContract {
mapping(address => uint256) myMapping;

function setValue(uint256 newValue) public {
myMapping[msg.sender] = newValue;
}

function getValue(address userAddress) public view returns (uint256) {
return myMapping[userAddress];
}
}

In this example, we define a mapping called "myMapping" that maps Ethereum addresses to uint256 values. The "setValue" function allows a value to be added to the mapping for the address of the current user, and the "getValue" function allows the value for a given address to be retrieved from the mapping.

Strings

(represents a variable-length string of characters.)

pragma solidity ^0.8.0;

contract ExampleContract {
string myString;

function setString(string memory newValue) public {
myString = newValue;
}

function getString() public view returns (string memory) {
return myString;
}
}

In this example, we define a string variable called "myString". The "setString" function allows a new string value to be assigned to "myString", and the "getString" function returns the value of "myString".


Note: There are two types of Data Types:

Value Data types and Reference data types.

To group related data together in a structured and organized way, we use Data Structures:

Examples of data structures in Solidity include arrays, structs, mappings, and enums. Data structures can contain both value data types and reference data types, and are typically used to create more complex data models for smart contracts.

Examples of an Array containing value and reference data type:

pragma solidity ^0.8.0;

contract ExampleContract {
uint256[] myUintArray;
string[] myStringArray;

function addValue(uint256 newValue, string memory newString) public {
myUintArray.push(newValue);
myStringArray.push(newString);
}

function getValue(uint256 index) public view returns (uint256, string memory) {
return (myUintArray[index], myStringArray[index]);
}
}

In this example, we define two dynamic arrays: "myUintArray" of type uint256, and "myStringArray" of type string. The "addValue" function allows new values to be added to the arrays, with one uint256 value and one string value added at a time. The "getValue" function allows the values of both arrays at a given index to be retrieved together, with a tuple containing one uint256 value and one string value returned.
Here, "myUintArray" is an example of an array containing a value data type (uint256), while "myStringArray" is an example of an array containing a reference data type (string).

Other Types of syntax includes:

Inheritance, Events, Functions, modifiers, contracts and control structures.

More sources to sharpen your skills 👇

## The Purpose Of Smart Contracts
*[⌨️ (00:18:27) The Purpose of Smart Contracts](https://youtu.be/gyMwXuJrbJQ?t=1107)*
- 🎥 [Original Video](https://www.youtube.com/watch?v=_JeRq7Gwj5Y&feature=youtu.be)
- 🦬 [My ETH Denver Talk](https://www.youtube.com/watch?v=06hXCX_jj2E)
- 🍔 [McDonalds Scandal](https://www.chicagotribune.com/sns-mcdonalds-story.html)
- ⛓ [More on the evolution of agreements](https://www.youtube.com/watch?v=ufVyX7JDCgg)
- ✍️ [What is a Smart Contract?](https://www.youtube.com/watch?v=ZE2HxTmxfrI)
- 🧱 [How does a blockchain work?](https://www.youtube.com/watch?v=SSo_EIwHSd4)
- 🔮 [Chainlink & Oracles](https://www.youtube.com/watch?v=tIUHQ7sDoaU)

## Other Blockchain Benefits
*[⌨️ (00:30:41) Other Blockchain Benefits](https://youtu.be/gyMwXuJrbJQ?t=1841)*
- Decentralized
- Transparency & Flexibility
- Speed & Efficiency
- Security & Immutability
- Counterparty Risk Removal
- Trust Minimized Agreements

## What have Smart Contracts done so far?
*[⌨️ (00:36:36) What have Smart Contracts done so far?](https://youtu.be/gyMwXuJrbJQ?t=2196)*
- [DeFi](https://chain.link/education/defi)
  - [Defi Llama](https://defillama.com/)
  - [Why DeFi is Important](https://medium.com/the-capital/why-defi-1519cc4d4bd3)
- [DAOs](https://betterprogramming.pub/what-is-a-dao-what-is-the-architecture-of-a-dao-how-to-build-a-dao-high-level-d096a97162cc)
- [NFTs](https://www.youtube.com/watch?v=9yuHz6g_P50)

## Making Your First Transaction
*[⌨️ (00:39:17) Making Your First Transaction](https://youtu.be/gyMwXuJrbJQ?t=2357)*
-   [Metamask Download Link](https://metamask.io/)
    -   [What is a Private Key?](https://www.coinbase.com/learn/crypto-basics/what-is-a-private-key)
    -   [What is a Secret Phrase?](https://metamask.zendesk.com/hc/en-us/articles/360060826432-What-is-a-Secret-Recovery-Phrase-and-how-to-keep-your-crypto-wallet-secure)
-   [Etherscan](https://etherscan.io/)
-   [Sepolia Etherscan](https://sepolia.etherscan.io/)
-   Sepolia Faucet (Check the [link token contracts page](https://docs.chain.link/docs/link-token-contracts/#sepolia))
    -   NOTE: The Chainlink documentation always has the most up to date faucets on their [link token contracts page](https://docs.chain.link/docs/link-token-contracts/#sepolia). If the faucet above is broken, check the chainlink documentation for the most up to date faucet.
-   OR, use the [Sepolia ETH Faucet](https://faucets.chain.link/), just be sure to swap your metamask to Sepolia!

## Gas I: Introduction to Gas
*[⌨️ (00:58:59) Gas I: Introduction to Gas](https://youtu.be/gyMwXuJrbJQ?t=3539)*
-   [Gas and Gas Fees](https://ethereum.org/en/developers/docs/gas/)
-   [Wei, Gwei, and Ether Converter](https://eth-converter.com/)
-   [ETH Gas Station](https://ethgasstation.info/)

## How Do Blockchains Work?
*[⌨️ (01:05:32) How Do Blockchains Work](https://youtu.be/gyMwXuJrbJQ?t=3932)*
- [What is a hash?](https://techjury.net/blog/what-is-cryptographic-hash/)
- [Blockchain Demo](https://andersbrownworth.com/blockchain/)
- [Summary](https://ethereum.org/en/developers/docs/intro-to-ethereum/)

## Signing Transactions
*[⌨️ (01:22:55) Signing Transactions](https://youtu.be/gyMwXuJrbJQ?t=4975)*
-   [Public / Private Keys](https://andersbrownworth.com/blockchain/public-private-keys/keys)
-   [Layer 2 and Rollups](https://ethereum.org/en/developers/docs/scaling/layer-2-rollups/)
-   [Decentralized Blockchain Oracles](https://blog.chain.link/what-is-the-blockchain-oracle-problem/)

## Gas II
*[⌨️ (01:30:22) Gas II: Block Rewards & EIP 1559](https://youtu.be/gyMwXuJrbJQ?t=5422)*
-   [Block Rewards](https://www.investopedia.com/terms/b/block-reward.asp)
-   Advanced Gas
    -   [EIP 1559](https://www.youtube.com/watch?v=MGemhK9t44Q)
    -   GWEI, WEI, and ETH
        -   [ETH Converter](https://eth-converter.com/)
## Gas II Summary
*[⌨️ (01:36:44) Gas II Summary](https://youtu.be/gyMwXuJrbJQ?t=5804)*
-   [Run Your Own Ethereum Node](https://geth.ethereum.org/docs/getting-started)

## High-Level Blockchain Fundamentals
*[⌨️ (01:39:32) High-Level Blockchain Fundamentals]https://www.youtube.com/watch?v=gyMwXuJrbJQ&t=5972s()*
-   [Consensus](https://wiki.polkadot.network/docs/learn-consensus)
-   [Proof of Stake](https://ethereum.org/en/developers/docs/consensus-mechanisms/pos/)
-   [Proof of Work](https://ethereum.org/en/developers/docs/consensus-mechanisms/pow/)
-   [Nakamoto Consensus](https://blockonomi.com/nakamoto-consensus/)
-   [Ethereum 2 (the merge)](https://ethereum.org/en/eth2/)

🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊 Completed Blockchain Basics! 🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊 

# Lesson 2: [Welcome to Remix! Simple Storage](https://github.com/PatrickAlphaC/simple-storage-fcc)

*[⌨️ (02:01:16) Lesson 2: Welcome to Remix! Simple Storage](https://www.youtube.com/watch?v=gyMwXuJrbJQ&t=7276s)*

💻 Code: https://github.com/PatrickAlphaC/simple-storage-fcc

## Introduction
*[⌨️ (02:03:05) Introduction](https://youtu.be/gyMwXuJrbJQ?t=7385)*
- [Remix](https://remix.ethereum.org/)
- [Solidity Documentation](https://docs.soliditylang.org/en/latest/index.html)

## Setting Up Your First Contract
*[⌨️ (02:05:18) Setting Up Your First Contract](https://youtu.be/gyMwXuJrbJQ?t=7518)*
-   Versioning
-   Take notes in your code!
-   [What is a software license](https://snyk.io/learn/what-is-a-software-license/)
-   SPDX License
-   Compiling
-   Contract Declaration

## Basic Solidity: Types
*[⌨️ (02:12:28) Basic Solidity Types](https://youtu.be/gyMwXuJrbJQ?t=7948)*
-   [Types & Declaring Variables](https://docs.soliditylang.org/en/v0.8.13/)
    -   `uint256`, `int256`, `bool`, `string`, `address`, `bytes32`
    -   [Solidity Types](https://docs.soliditylang.org/en/latest/types.html)
    -   [Bits and Bytes](https://www.youtube.com/watch?v=Dnd28lQHquU)
-   Default Initializations
-   Comments

## Basic Solidity: Functions
*[⌨️ (02:18:40) Basic Solidity Functions](https://youtu.be/gyMwXuJrbJQ?t=8320)*
-   Functions
-   Deploying a Contract
    -   Smart Contracts have addresses just like our wallets
-   Calling a public state-changing Function
-   [Visibility](https://docs.soliditylang.org/en/latest/contracts.html#visibility-and-getters)
-   Gas III | An example
-   Scope
-   View & Pure Functions

## Basic Solidity: Arrays & Structs
*[⌨️ (02:35:30) Basic Solidity Arrays & Structs](https://youtu.be/gyMwXuJrbJQ?t=9331)*
-   Structs
-   Intro to Storage
-   Arrays 
-   Dynamic & Fixed Sized
-   `push` array function


## Basic Solidity: Compiler Errors and Warnings
*[⌨️ (02:45:35) Basic Solidity Errors & Warnings](https://youtu.be/gyMwXuJrbJQ?t=9935)*
- Yellow: Warnings are Ok
- Red: Errors are not Ok

## Memory, Storage, Calldata (Intro)
*[⌨️ (02:46:34) Basic Solidity Memory, Storage, & Calldata (Intro)](https://youtu.be/gyMwXuJrbJQ?t=9994)*
- 6 Places you can store and access data
  - calldata
  - memory
  - storage
  - code
  - logs
  - stack

## Mappings
*[⌨️ (02:50:17) Basic Solidity Mappings](https://youtu.be/gyMwXuJrbJQ?t=10217)*
- [Mappings](https://solidity-by-example.org/mapping)

## Deploying your First Contract
*[⌨️ (02:53:38) Deploying your First Contract](https://youtu.be/gyMwXuJrbJQ?t=10418)*
-   A testnet or mainnet
-   Connecting Metamask
-   [Find a faucet here](https://docs.chain.link/docs/link-token-contracts/#Sepolia)
-   See the faucets at the top of this readme!
-   Interacting with Deployed Contracts

## The EVM & A Recap of Lesson 2
*[⌨️ (03:03:07) The EVM & A Recap of Lesson 2](https://youtu.be/gyMwXuJrbJQ?t=10987)*
-   The EVM

# Lesson 3: Remix Storage Factory

*[⌨️ (03:05:34) Lesson 3: Remix Storage Factory](https://www.youtube.com/watch?v=gyMwXuJrbJQ&t=11134s)*

💻 Code: https://github.com/PatrickAlphaC/storage-factory-fcc

## Introduction
*[⌨️ (03:06:06) Introduction](https://youtu.be/gyMwXuJrbJQ?t=11166)*
- [Factory Pattern](https://betterprogramming.pub/learn-solidity-the-factory-pattern-75d11c3e7d29)

## Basic Solidity: Importing Contracts into other Contracts
*[⌨️ (03:07:29) Importing Contracts into other Contracts](https://youtu.be/gyMwXuJrbJQ?t=11249)*
- [Composibility](https://chain.link/techtalks/defi-composability)
- [Solidity new keyword](https://docs.soliditylang.org/en/latest/control-structures.html?highlight=new#creating-contracts-via-new)
- [Importing Code in solidity](https://solidity-by-example.org/import)

## Basic Solidity: Interacting with other Contracts
*[⌨️ (03:16:36) Interacting with other contracts](https://youtu.be/gyMwXuJrbJQ?t=11796)*
- To interact, you always need: ABI + Address
- [ABI](https://docs.soliditylang.org/en/latest/abi-spec.html?highlight=abi)

## Basic Solidity: Inheritance & Overrides
*[⌨️ (03:25:23) Inheritance & Overrides](https://youtu.be/gyMwXuJrbJQ?t=12323)*
- [Inheritance](https://solidity-by-example.org/inheritance) 
- [Override & Virtual Keyword](https://docs.soliditylang.org/en/latest/contracts.html?highlight=override#function-overriding)

## Lesson 3 Recap
*[⌨️ (03:30:29) Lesson 3 Recap](https://youtu.be/gyMwXuJrbJQ?t=12629)*
