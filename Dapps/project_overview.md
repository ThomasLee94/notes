# Dapps project overview

- Solidity Contract
- Solidity Compiler => ABI, Bytecode

- ABI is needed to communicate with Web3
- Bytecode is needed to deploy onto network (main, rinkeby etc)

## Compile

- import solidity compiler
- read in contract
- compile the contract(s)
- export bytecode

## Tests

- Import Web3, how we communicate with the network we deployed too.
- Give web3 a provider (which network it needs to communicate with)
- Use Ganache-cli for provider, a local test network.
- Import interface (ABI)
- import bytecode (Compiled contract)
- Mocha for tests
    - use beforeEach to get a fresh copy of the contract
    - use it statements to test each feature (use methods object to get access to all functions from contract)
        - call contract_function_name().call() or contract_function_name().send()
            - .send() takes a while and you need to provide gas
    

## Deploy

- import HDWalletProvider (provider)
    - this is needed to connect with some target network and unlock an account for use on that network.
        - unlock with 12 word mnmemonic (MetaMask) => can unlock public, private key and address of account.
        - Give Infura Node address. 
- give provider mnmemonic and Infura URL.
- Import web3 to get a list of all of our accounts.
- deploy contract