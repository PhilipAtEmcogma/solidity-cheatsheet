# solidity-cheatsheet
 # usful command on CLI for solidity
 # 1. include above pragma in all the smart contract files, note: MIT is open licence, need to change to something if the conract isn't intented to be a open liscence smart contact.
 ## // SPDX-License-Identifier: MIT

# 2. if using Truffle to deploy smart contracts in solidity (note: I only tried it in Window's VSCode, might need to tweak it if using other OS and/or editor):
## i) initialising truffle, this would create some folders and files in your project, make sure to initialise truffle in the root of the project
###   truffle init
## ii) start local (on the machine) EVM, so can deploy contracts locally to test and play round, without the need to deploy it the mainnet.  Note: EVM will also generate some wallets and its seed phrase for me to use.  but these wallets are ofcourse only for local EVM and should not be use for mainnet.  code:
###     truffle develop
## iii) compile contracts
###   truffle compile
## iV) deploying (migrating) the contract, note in the migrations folder, naming conventions goes by x_name_description.js, where x is number starting from one and increase by 1 for each new iteration and truffle will automatically choose the latest (biggest number) migration file to depoly, e.g. 1_initial_migrations.js, 2_token_migrations.js, truffle will always run 2_token_migrations.js when migrate command is called:
###   truffle migrate
##  or do this if running on a local EVM:
### migrate
## side note: in the migration file, make sure to use the name of the actual contract, NOT the name of the file that holds the contract
# 3. ERC165 tutorial read: https://medium.com/@chiqing/ethereum-standard-erc165-explained-63b54ca0d273

## RPC-URL
### To connect to and retrieve data from a blockchain, you'll need to connect to a node on the blockchain network. A node is a participant in the network that stores and serves the latest blockchain state. Users who wish to download blockchain data can either run a node themselves, or connect to a publicly-provided node via the node's RPC endpoint. An RPC (remote procedure call) endpoint is like a node's address: it's a URL which requests for blockchain data can be sent to.
### Alchemy RPC-URL doc: https://docs.alchemy.com/docs/how-to-add-alchemy-rpc-endpoints-to-metamask
### Alchemy website: https://www.alchemy.com/