#By_Rishabh-singh
#Ride-Fair
Decentralized ride sharing on the Ethereum blockchain.
The project contains the frontend website and backend Ethereum Smart Contract to deploy and run the decentralized ride sharing application.

## Smart contract
* The `backend/ridefair.sol` file contains the logic for all interaction between rider and driver orchestrated on the blockchain run on an Ethereum test network.

## Ganache test Network
* Ganache (https://www.trufflesuite.com/ganache) is used as the test network to deploy the `ridefair.sol` smart contract on.
* Once ganache is installed, a test network is started using `quickstart`. The default test network start on local host at port number 7545 (http://127.0.0.1:7545)
* The `backend/mig.js` script can be used to deploy the contract onto the ganache test network.
* Make sure to have the right network address and contract deployer enthereum address (from address) set to deploy the contract correctly on the Ganache test network instance.
* If the `mig.js` file is giving problems in deployment, the Remix IDE (https://remix.ethereum.org/) can also be used to deploy the contract on the ganache test network instance. Again make sure to have the right network address selected.
* If Both the above method don't work then use truffle package option I have made every thing ready first open the `truffle-config.js` as project into ganache and just open the backend folder and run `truffle migrate` command your ridefair.sol file would be compiled and deployed over ganche.(`I have used this method because i find it easy to implement and deploy over other methods`)
* Be sure to note down the address and paste it to the `App.js` at which the contract was deployed at.

## React application
* A frontend React webpage is used to facilitate user interaction with the blockchain.
* To install required packages run `npm install` in the `frontend` folder.
* Be sure to have the contract address of the previously deployed smart contract set correctly in the `frontend/src/App.js` file so the React application can communicate with the previously deployed contract.
* Also make sure to have the right network address set in `frontend/src/js_modules/contractInterface.js` so the application is connecting the the ganache test network previously deployed.
* Running the `npm run start` command in teh `frontend` folder should start up the React application
