# Decentralized Voting (dVoting)

A decentralized voting system based on Ethereum blockchain technology.


## System Workflow

A brief explanation on the basic workflow of the application.

- Admin will create a voting instance by launching/deploying the system in a blockchain network, then create an election instance and start the election with the details of the election filled in (including candidates for voters to vote).
- Then the voters will connect to the same blockchain network register to become a voter. Once the users successfully register, their respective details are sent/displayed in the admins' panel (i.e. verification page).
- The admin then will check if the registration information (blockchain account address, name, and phone number) is valid. If yes, then the admin approves the registered user making them eligible to take part and cast their respective vote in the election.
- The registered user (voter) following the approval from the admin casts their vote to the candidate of interest (from the voting page).
- After some time, depending on the scale of the election the admin ends the election. As that happens the voting is closed and the results are displayed announcing the winner at the top of the results page.


---

## Setting up the development environment

### Requirements

- [Node.js](https://nodejs.org)
- [Truffle](https://archive.trufflesuite.com/docs/truffle/how-to/install/#install-truffle)
- [Ganache](https://archive.trufflesuite.com/ganache/)
- [Metamask](https://metamask.io/) (Browser Extension)

#### Getting the requirements

1. Download and install **NodeJS**

   Download and install NodeJS from [here](https://nodejs.org/en/download/). 

1. Install **truffle** and **ganache-cli** using node packager manager (npm)

   ```shell
   npm install -g truffle
   npm install -g ganache-cli
   ```

1. Install **metamask** browser extension

   Download and install metamask from [here](https://metamask.io/download).

### Configuring the project for development

1. Run local Ethereum blockchain

   ```shell
   ganache
   ```

   > Note: Do not close `ganache` (the blockchain network needs to be running all the time)

1. Configure metamask on the browser with the following details

   New RPC URL: from Ganache (update it in the file:`truffle-config.js` as well)*

   Chain ID: `1337`

1. Import account(s) using private keys from ganache-cli to the metamask extension on the browser

1. Deploy smart contract to the (local) blockchain network (i.e ganache)

   ```shell
   # on the dVoting directory
   truffle migrate
   ```

   > Note: Use `truffle migrate --reset` for re-deployments

1. Launch the development server (frontend)

   ```shell
   cd client
   npm install
   npm start
   ```



