
# Ophir Solidity-Smartcontract-Class

Welcome to the repository for the Ophir Solidity-Smartcontract-Class - Beginner to Expert Full Course | by Ophir!

Recommended Testnet: Sepolia


<i>We have create the repos to work with Sepolia due to Rinkeby and Kovan being sunset, and Goerli being a disaster. Let us know if yo have any issues!</i>


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

## Comments:

Solidity supports both:

1. single-line comments ``(denoted by "//")``

2. multi-line comments ``(denoted by "/* ... */").``

## Variables:

Solidity supports several data types for variables, including:

## Value data types:

### Boolean- bool,

(represents true or false values.)

``pragma solidity ^0.8.0;``

``contract ExampleContract {``
``bool myBool = true;``

``function getBool() public view returns (bool) {``
``return myBool;``
``}``
``}``

<i>In this example, we define a boolean variable "myBool" and initialize it to true. The "getBool" function returns the value of "myBool".</i>




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

<i>In this example, we define an integer variable "myInt" and initialize it to -123, and an unsigned integer variable "myUint" and initialize it to 456. The "getInt" function returns the value of "myInt", and the "getUint" function returns the value of "myUint".</i>

### fixed point numbers - fixed,

(represents decimal numbers with a fixed number of digits.)

``pragma solidity ^0.8.0;``

``1contract ExampleContract {``
``fixed256x18 myFixed = 123.456;``

``function getFixed() public view returns (fixed256x18) {``
``return myFixed;``
``}``
``}``

<i>In this example, we define a fixed point number variable "myFixed" with 18 decimal places and initialize it to 123.456. The "getFixed" function returns the value of "myFixed".</i>

### Address- address,

(represents an Ethereum address.)

``pragma solidity ^0.8.0;``

``contract ExampleContract {``
``address payable myAddress = payable(0x1234567890123456789012345678901234567890);``

``function getAddress() public view returns (address payable) {``
``return myAddress;``
``}``
``}``

<i>In this example, we define an address variable "myAddress" and initialize it to the Ethereum address "0x1234567890123456789012345678901234567890". The "getAddress" function returns the value of "myAddress".</i>


### bytes,

(represents a single byte of data.)

``pragma solidity ^0.8.0;``

``contract ExampleContract {``
``bytes32 myBytes = hex"00112233445566778899aabbccddeeff";``

``function getBytes() public view returns (bytes32) {``
``return myBytes;``
``}``
``}``

<i>In this example, we define a bytes variable "myBytes" and initialize it to the hex value "00112233445566778899aabbccddeeff". The "getBytes" function returns the value of "myBytes".</i>



### Enums

(represents a set of named constants.)


``pragma solidity ^0.8.0;``

``contract ExampleContract {``
``enum State { New, InProgress, Completed }``
``State myState = State.New;``

``function getState() public view returns (State) {``
``return myState;``
``}``
``}``

<i>In this example, we define an enum "State" with three possible values: "New", "InProgress", and "Completed". We also define an enum variable "myState" and initialize it to "New". The "getState" function returns the value of "myState".</i>


<i>Variables can be declared using the syntax "type name = value;".</i>

## Reference data types:



### Arrays

(Solidity supports both fixed-size and dynamic arrays, which can be of any data type.)

``pragma solidity ^0.8.0;``

``contract ExampleContract {``
``uint256[] myArray;``

``function addValue(uint256 newValue) public {``
``myArray.push(newValue);``
``}``

``function getValue(uint256 index) public view returns (uint256) {``
``return myArray[index];``
``}``
``}``

<i>In this example, we define an empty dynamic array of uint256 values called "myArray". The "addValue" function allows values to be added to the array, and the "getValue" function allows values to be retrieved from the array using an index value</i>

### Structs

(Structs are used to group related data together. They can contain multiple data types, including other structs or arrays.)

``pragma solidity ^0.8.0;``

``contract ExampleContract {``
``struct Person {``
``string name;``
``uint256 age;``
``}``

``Person myPerson;``

``function setPerson(string memory newName, uint256 newAge) public {``
``myPerson = Person(newName, newAge);``
``}``

``function getPerson() public view returns (string memory, uint256) {``
``return (myPerson.name, myPerson.age);``
``}``
``}``

<i>In this example, we define a struct "Person" with two fields: "name" and "age". We then define a variable "myPerson" of type "Person". The "setPerson" function allows a new Person object to be created and assigned to "myPerson", and the "getPerson" function returns the values of "myPerson"'s "name" and "age" fields.</i>

### Mappings:

(Mappings are used to create key-value pairs, similar to dictionaries or hash tables in other languages. They are particularly useful for creating data lookups.)

``pragma solidity ^0.8.0;``

``contract ExampleContract {``
``mapping(address => uint256) myMapping;``

``function setValue(uint256 newValue) public {``
``myMapping[msg.sender] = newValue;``
``}``

``function getValue(address userAddress) public view returns (uint256) {``
``return myMapping[userAddress];``
``}``
``}``

<i>In this example, we define a mapping called "myMapping" that maps Ethereum addresses to uint256 values. The "setValue" function allows a value to be added to the mapping for the address of the current user, and the "getValue" function allows the value for a given address to be retrieved from the mapping.</i>

### Strings

(represents a variable-length string of characters.)

``pragma solidity ^0.8.0;``

``contract ExampleContract {``
``string myString;``

``function setString(string memory newValue) public {``
``myString = newValue;``
``}``

``function getString() public view returns (string memory) {``
``return myString;``
``}``
``}``

<i>In this example, we define a string variable called "myString". The "setString" function allows a new string value to be assigned to "myString", and the "getString" function returns the value of "myString".</i>


<i> Note: There are two types of Data Types:

Value Data types and Reference data types.

To group related data together in a structured and organized way, we use Data Structures:

Examples of data structures in Solidity include arrays, structs, mappings, and enums. Data structures can contain both value data types and reference data types, and are typically used to create more complex data models for smart contracts.</i>

Examples of an Array containing value and reference data type:

``pragma solidity ^0.8.0;``

``contract ExampleContract {``
``uint256[] myUintArray;``
``string[] myStringArray;``

``function addValue(uint256 newValue, string memory newString) public {``
``myUintArray.push(newValue);``
``myStringArray.push(newString);``
``}``

``function getValue(uint256 index) public view returns (uint256, string memory) {``
``return (myUintArray[index], myStringArray[index]);``
``}``

``}``

<i>In this example, we define two dynamic arrays: "myUintArray" of type uint256, and "myStringArray" of type string. The "addValue" function allows new values to be added to the arrays, with one uint256 value and one string value added at a time. The "getValue" function allows the values of both arrays at a given index to be retrieved together, with a tuple containing one uint256 value and one string value returned.
Here, "myUintArray" is an example of an array containing a value data type (uint256), while "myStringArray" is an example of an array containing a reference data type (string).</i>

Other Types of syntax includes:

Inheritance, Events, Functions, modifiers, contracts and control structures.

More sources to sharpen your skills 👇

## Introduction to Ethereum Network

Ethereum is a decentralized, open-source blockchain with smart contract functionality. Ether is the native cryptocurrency of the platform.

Among cryptocurrencies, ether is second only to bitcoin in market capitalization. Ethereum was conceived in 2013 by programmer Vitalik Buterin.



## Understanding of blockchain and smart contracts

## Introduction to Smartcontracts

Smart contracts are self-executing digital contracts that run on a blockchain platform, and are programmed to automatically execute the terms of the contract when certain conditions are met.

Smart contracts are written in programming languages, and Solidity is one of the most popular languages used for writing smart contracts on the Ethereum blockchain.

Smart contracts are used in Solidity to automate the exchange of assets between parties without the need for a middleman or trusted third party.

This makes them ideal for applications such as crowdfunding, escrow services, and other types of financial transactions where trust is important.

### One example of a smart contract is an escrow contract:

<i> An escrow contract is a type of smart contract that holds funds in escrow until certain conditions are met.

For example, in a real estate transaction, an escrow contract could be used to hold the purchase price of the property until the buyer has completed all necessary inspections and due diligence, at which point the funds would be released to the seller.

In Solidity, an escrow contract could be written using a combination of state variables, functions, and events to define the terms of the contract, as well as a mapping to track the funds held in escrow </i>


### Another example of a smart contract is a crowdfunding contract:

<i> A crowdfunding contract is a type of smart contract that allows multiple parties to pool their resources to support a common goal or project.

For example, a crowdfunding contract could be used to raise funds for a new business venture, with investors receiving a share of the profits if the venture is successful.

In Solidity, a crowdfunding contract could be written using a combination of state variables, functions, and events to define the terms of the contract, as well as a mapping to track the contributions made by each investor for example the fund me smart contract below 👇 </i>


### For more information on SmartContracts watch this video:

[Welcome to Remix! Ophir Bank](https://drive.google.com/drive/folders/1MJFRLXTW1zgZbnYI2FyNGgnINxaCLJXP)

<i>[⌨️ (04:21:94) : Welcome to Remix! Ophir Bank](https://github.com/OphirInstitute/Remix-fundme)</i>



## Introduction to Blockchain

### -What exactly is a blockchain?

A blockchain is a distributed ledger technology.

The Word “Ledger”means A book or other collections of financial transactions.

The Word “Distributed” denotes Location.

So it basically means that these ledgers are stored in different locations & these locations are Reffered to as Nodes.

While ledger is continuously updated and validated through consensus algorithms.

### Types of Blockchains

Centralized blockchains
Decentralized blockchains
Hybrid blockchains
Consortium blockchains

### Centralized Blockchains-

These are blockchains that have a central authority controls the whole process(read, write and validate transactions (

Transactions are malleable ( it can be deleted), they are known as permissioned blockchains.

Used in banks for private and restricted purposes.

Used in the government for keeping private data like tax records

### Decentralized Blockchains-

Decentralized blockchains are a type of distributed ledger technology (DLT) that allows multiple parties to maintain a shared, tamper-proof database without the need for a central authority. Instead, the blockchain uses a network of computers, known as nodes, to verify and record transactions.

It is immutable, Transparent and secure.

Applications vary widely in crypto currency transactions, supply chain management, voting systems and more

Bitcoin facilities peer to peer transactions

Examples of decentralized blockchains in crypto: Ethereum and litecoin


### Hybrid Blockchains

This is the combination of both public and centralized blockchains.

In this case an aspect of the blockchain is for the public to interact while the other is restricted or permissioned.

Examples are Ripple and hyper ledger.

<i>They Offer a balance between the transparency and security of public blockchains and control and privacy of private blockchains.</i>

### Consortium Blockchains

Termed as a form of “Decentralized Control”

By groups of organizations they work together to validate transactions.

It allows for privacy and still operates in a decentralized fashion it is mostly used in the supply chain industry.

Examples include:

<i>R3 Corda Platform
Enterprise Ethereum Alliance</i>

















