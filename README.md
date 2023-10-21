# Truffle Suite

Decentralized application(Dapp): Adoption tracking system for a pet shop

---

### Truffle Overview

Truffle is a collection of tools that simplifies the development of **blockchain-based** applications on **EVM-compatible networks**(EVM: Ethereum Virtual Machine). It focuses on the development of **smart contracts**, which are the foundation of EVM applications.

[**Ganache](https://trufflesuite.com/ganache):** personal blockchain for **Ethereum** development you can use to deploy contracts, develop applications, and run tests.

---

### **Setting up the development environment**

**Technical Requirements**

![Untitled](assets/Untitled.png)

**Installing Truffle**

![Untitled](assets/Untitled%201.png)

![Untitled](assets/Untitled%202.png)

---

### **Creating a Truffle project using a Truffle Box**

Truffle Box : pre-configured **project template** that provides a foundation for developing decentralized applications (DApps) on the Ethereum blockchain using the Truffle framework. These boxes come with a pre-defined directory structure, smart contracts, tests, and often include front-end code as well.

- Unboxing a truffle box called **“pet-shop”**

![Untitled](assets/Untitled%203.png)

This is the project’s folder structure 

![Untitled](assets/Untitled%204.png)

- `contracts/`: Contains the [Solidity](https://solidity.readthedocs.io/) source files for our smart contracts. There is an important contract in here called `Migrations.sol`
- `migrations/`: Truffle uses a migration system to handle smart contract deployments. A migration is an additional special smart contract that keeps track of changes.
- `test/`: Contains both JavaScript and Solidity tests for our smart contracts
- `truffle-config.js`: Truffle configuration file

---

### **Writing the smart contract**

`Adoption.sol` : back-end logic and storage

Every account and smart contract on the **Ethereum** blockchain has an address and can send and receive Ether to and from this **address**.

First, we created an Ethereum address 

Then, we wrote 2 functions

![Untitled](assets/Untitled%205.png)

---

### Compilation

![Untitled](assets/Untitled%206.png)

⇒ Compiled successfully 

---

### Migration

- Migrating the smart contracts to the blockchain
- **A migration is a deployment script meant to alter the state of your application's contracts**, moving it from one state to the next.
- `1_initial_migration.js:`handles deploying the `Migrations.sol` contract to observe subsequent smart contract migrations, and ensures we don't double-migrate unchanged contracts in the future.

**Downloading Ganache** 

![Untitled](assets/Untitled%207.png)

**Migrating** 

![Untitled](assets/Untitled%208.png)

![Untitled](assets/Untitled%209.png)

⇒ migrations executed in order

![Untitled](assets/Untitled%2010.png)

**Note :** The blockchain now shows that the current block, previously `0`, is now `4`. In addition, while the first account originally had 100 ether, it is now lower, due to the transaction costs of migration.

---

### **Testing the smart contract using Solidity**

![Untitled](assets/Untitled%2011.png)

---

### Testing the smart contract using Javascript

![Untitled](assets/Untitled%2012.png)

---

### Running the test

![Untitled](assets/Untitled%2013.png)

![Untitled](assets/Untitled%2014.png)

---

### **Creating a user interface to interact with the smart contract**

Downloading **Metamask** extension 

![Untitled](assets/Untitled%2015.png)

![Untitled](assets/Untitled%2016.png)

We then created a new **network** : Ganache [localhost:7545](http://localhost:7545) 

![Untitled](assets/Untitled%2017.png)

**Note : Each account created by Ganache is given 100 ether. It's slightly less on the first account because some gas was used when the contract itself was deployed and when the tests were run.**

![Untitled](assets/Untitled%2018.png)

**⇒ The Configuration is now complete.**

---

### **Installing and configuring lite-server**

- `lite-server` library : serve our static files. This shipped with the `pet-shop` Truffle Box

![Untitled](assets/Untitled%2019.png)

⇒ This tells `lite-server` which files to include in our base directory. We add the `./src` directory for our website files and `./build/contracts` directory for the contract artifacts.

![Untitled](assets/Untitled%2020.png)

This tells npm to run our local install of `lite-server` when we execute `npm run dev` from the console.

---

### Using the dapp

- Start the local web server

![Untitled](assets/Untitled%2021.png)

[localhost:3000](http://localhost:3000) 

![Untitled](assets/Untitled%2022.png)

A **MetaMask** pop-up should appear requesting your approval to allow Pete's Pet Shop to connect to your **MetaMask** wallet.

![Untitled](assets/Untitled%2023.png)

After clicking the **Adopt** button on the pet of your choice

![Untitled](assets/Untitled%2024.png)

The button says **“Success”,** and in **MetaMask**

![Untitled](assets/Untitled%2025.png)

And in **Ganache**

![Untitled](assets/Untitled%2026.png)
![Untitled](assets/Untitled%2027.png)