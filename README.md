prediction-markets-spam
=======================

Prediction markets for spam mitigation.

 * Frontend
 * Contracts
 * Subgraph

## Setup.

 1. Clone all submodules.
    
    ```sh
    git submodule update --init --recursive
    ```

 2. Install Hardhat. (and potentially [update your Metamask](https://github.com/MetaMask/metamask-extension/issues/9827))

 3. Run your Hardhat blockchain node.
    
    ```sh
    yarn hardhat node
    ```

 4. Install and run a local Graph node.

    ```sh
    cd graph-node/docker
    docker-compose up
    ```
 
 5. Deploy the omen-subgraph contracts and subgraph. 

    ```sh
    cd omen-subgraph/
    
    # Do this on 1st run.
    yarn create-local

    yarn codegen && yarn build && yarn deploy-local
    ```
  
  6. Deploy the curatem contracts.

    ```sh
    cd curatem-contracts/
     
    yarn
    yarn deploy
    ```
  
  7. Deploy the curatem subgraph.

    ```sh
    cd curatem-subgraph/
    
    # Do this on 1st run.
    yarn create-local

    yarn codegen && yarn build && yarn deploy-local
    ```
  
  8. Run the dApp.

    ```sh
    cd curatem-frontend/

    yarn
    yarn start
    ```

