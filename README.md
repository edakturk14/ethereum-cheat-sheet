# Ethereum Cheat Sheet 

Ethereum basics - Transactions, Accounts, EIPs &amp; more

## Terminology 

- Accounts: Externally owned accounts vs. Contract Accounts.  
- Transactions: cryptographically signed instrıctions from EOAs. 
    - The tx signature: proves that the tx came from the sender (signed with the senders private key)
    - An ethereum client like geth will handle the signing process
    - There are different types of tx: regular (tx from one account to another), contract deployment, execution of a contract
    - The tx lifecycle is: 1. A ts hash is generated --> 2. tx is broadcasted to the network and added to the tx pool --> 3. A validator must pick up your tx and include it in a block --> 4. the tx will become finalized once its included
- Gas: cost of the computation required to process a transaction. 
- Block: batches of transactions with a hash of the previous block in the chain.
- EVM: Ethereum Virtual Machine defines the rules for computing a new valid state
- Node: Instance of an ethereum client software that's connected to other computers. A node has two running clients: execution client and consensus client. 
    - There are different kind of nodes that you can run: full, light, archive node
        - Full:
        - Archive:
        - Light: Instead of downloading every block, light nodes only download block headers. The light nodes can not partiicpate in ethereum consensus however they can acess the blockchain with same functionality. 
    - Client diversity is a huge topic 
- Sequencer 
- Validator 
- PoS: In PoS validators have to stake 32 ETH as collateral. In every slot a validator is randomly selected to be the block proposer. The validator bundles the transactions together, execute them and determines the new "state." 
- PoW vs PoS: Proof-of-Stake (POS) uses randomly selected validators to confirm transactions and create new blocks. Proof-of-Work (POW) uses a competitive validation method to confirm transactions and add new blocks to the blockchain.
- Flashbots Protect: node thats does not track your ip
- Flashbots for Searchers: Connects searchers to validators while avoiding the public tx mempool. 

## EIP's
Ethereum Improvement Proposals's are standarts for potential new features or processes for Ethereum.

- 4844: Porto-danksharing: sub blockchains or shards
- 4337: Account Abstraction: single type of accounts. Upgrades EOAs so that they can be controlled by a smart contract (account recovery, batch tx) and also upgrading smart contract accounst so that they can initiate transactions.

## Optimisim 