# Truffle Suite

Decentralized application(Dapp): Adoption tracking system for a pet shop

---

### Truffle Overview

Truffle is a collection of tools that simplifies the development of **blockchain-based** applications on **EVM-compatible networks**(EVM: Ethereum Virtual Machine). It focuses on the development of **smart contracts**, which are the foundation of EVM applications.

[**Ganache](https://trufflesuite.com/ganache):** personal blockchain for **Ethereum** development you can use to deploy contracts, develop applications, and run tests.

---

### **Setting up the development environment**

**Technical Requirements**

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ba0a5610-a4a6-4894-badc-cf70f07abfe0/d35b922a-1559-41bf-92cf-90ebccf85edc/Untitled.png)

**Installing Truffle**

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ba0a5610-a4a6-4894-badc-cf70f07abfe0/60848977-07a9-4a2f-8d80-d27c93fac46a/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ba0a5610-a4a6-4894-badc-cf70f07abfe0/13953dae-fd56-47d1-8a34-4a3cc33f56a0/Untitled.png)

---

### **Creating a Truffle project using a Truffle Box**

Truffle Box : pre-configured **project template** that provides a foundation for developing decentralized applications (DApps) on the Ethereum blockchain using the Truffle framework. These boxes come with a pre-defined directory structure, smart contracts, tests, and often include front-end code as well.

- Unboxing a truffle box called **“pet-shop”**

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ba0a5610-a4a6-4894-badc-cf70f07abfe0/6bbb7998-339a-44e5-be5d-93b2095f0d50/Untitled.png)

This is the project’s folder structure 

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ba0a5610-a4a6-4894-badc-cf70f07abfe0/91face22-9c29-4b7c-911e-a2ec7ff11446/Untitled.png)

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

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ba0a5610-a4a6-4894-badc-cf70f07abfe0/85e91e0c-affd-4356-b7c1-d907a0f927ca/Untitled.png)

---

### Compilation

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ba0a5610-a4a6-4894-badc-cf70f07abfe0/11874221-f543-4346-83f8-1c463d701f43/Untitled.png)

⇒ Compiled successfully 

---

### Migration

- Migrating the smart contracts to the blockchain
- **A migration is a deployment script meant to alter the state of your application's contracts**, moving it from one state to the next.
- `1_initial_migration.js:`handles deploying the `Migrations.sol` contract to observe subsequent smart contract migrations, and ensures we don't double-migrate unchanged contracts in the future.

**Downloading Ganache** 

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ba0a5610-a4a6-4894-badc-cf70f07abfe0/ba50044e-6878-4a62-b054-197d32b7e69d/Untitled.png)

**Migrating** 

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ba0a5610-a4a6-4894-badc-cf70f07abfe0/dc4fec50-9bd1-4a95-8c0b-17ee2047569d/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ba0a5610-a4a6-4894-badc-cf70f07abfe0/b8ca3b73-72b3-4c9d-92ae-4c60a54dfac4/Untitled.png)

⇒ migrations executed in order

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ba0a5610-a4a6-4894-badc-cf70f07abfe0/a710e897-9c65-479b-9522-1c4c059512fc/Untitled.png)

**Note :** The blockchain now shows that the current block, previously `0`, is now `4`. In addition, while the first account originally had 100 ether, it is now lower, due to the transaction costs of migration.

---

### **Testing the smart contract using Solidity**

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ba0a5610-a4a6-4894-badc-cf70f07abfe0/a50aa563-6c89-4574-80e1-ce6584a17ffd/Untitled.png)

---

### Testing the smart contract using Javascript

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ba0a5610-a4a6-4894-badc-cf70f07abfe0/4bfcd2e6-35d4-4b33-867f-4b40f2b4d6cf/Untitled.png)

---

### Running the test

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ba0a5610-a4a6-4894-badc-cf70f07abfe0/ba9deb3f-fb18-4edb-9922-edc53e7ec83d/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ba0a5610-a4a6-4894-badc-cf70f07abfe0/3484caad-06e5-41c6-8f63-12d98eaa6c47/Untitled.png)

---

### **Creating a user interface to interact with the smart contract**

Downloading **Metamask** extension 

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ba0a5610-a4a6-4894-badc-cf70f07abfe0/b1ddb580-5b05-441c-b83e-722be9746848/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ba0a5610-a4a6-4894-badc-cf70f07abfe0/ce41aedf-0aa1-4471-a468-6f94e18bcab0/Untitled.png)

We then created a new **network** : Ganache [localhost:7545](http://localhost:7545) 

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ba0a5610-a4a6-4894-badc-cf70f07abfe0/403276a6-3d9c-4c1a-9705-1e94cc9ec4d7/Untitled.png)

**Note : Each account created by Ganache is given 100 ether. It's slightly less on the first account because some gas was used when the contract itself was deployed and when the tests were run.**

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ba0a5610-a4a6-4894-badc-cf70f07abfe0/30fb65ca-3036-4a82-8fff-5874e5352dbc/Untitled.png)

**⇒ The Configuration is now complete.**

---

### **Installing and configuring lite-server**

- `lite-server` library : serve our static files. This shipped with the `pet-shop` Truffle Box

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ba0a5610-a4a6-4894-badc-cf70f07abfe0/859144ef-9497-4173-9bce-3592b555fb20/Untitled.png)

⇒ This tells `lite-server` which files to include in our base directory. We add the `./src` directory for our website files and `./build/contracts` directory for the contract artifacts.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ba0a5610-a4a6-4894-badc-cf70f07abfe0/4e9b5c06-4f64-4ec4-b19f-1e13fb489701/Untitled.png)

This tells npm to run our local install of `lite-server` when we execute `npm run dev` from the console.

---

### Using the dapp

- Start the local web server

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ba0a5610-a4a6-4894-badc-cf70f07abfe0/30e65257-ea04-4eae-b25c-82dc983f99c7/Untitled.png)

[localhost:3000](http://localhost:3000) 

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ba0a5610-a4a6-4894-badc-cf70f07abfe0/35c1354d-1ddf-47a2-a483-ccfb1662098b/Untitled.png)

A **MetaMask** pop-up should appear requesting your approval to allow Pete's Pet Shop to connect to your **MetaMask** wallet.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ba0a5610-a4a6-4894-badc-cf70f07abfe0/1f4961c3-9713-44a0-a65d-488c027a4c55/Untitled.png)

After clicking the **Adopt** button on the pet of your choice

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ba0a5610-a4a6-4894-badc-cf70f07abfe0/aa06fad4-c389-48cc-adfa-2a7113c910b5/Untitled.png)

The button says **“Success”,** and in **MetaMask**

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ba0a5610-a4a6-4894-badc-cf70f07abfe0/c024db65-9649-4bc0-95b6-10c4254924b3/Untitled.png)

And in **Ganache**