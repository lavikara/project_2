#### ERC-721 Token Name

```Lavi Token```
   
#### ERC-721 Token Symbol

```Lavi```

#### Contract address on rinkeby

```0xB4CFe8eE04CbA3e729d93B70c87aeFA0bc2be8fd```



### OpenZeppelin version used in the project.

```
"openzeppelin-solidity": {
   "version": "2.3.0",
   "resolved": "https://registry.npmjs.org/openzeppelin-solidity/-/openzeppelin-solidity-2.3.0.tgz",
   "integrity": "sha512-QYeiPLvB1oSbDt6lDQvvpx7k8ODczvE474hb2kLXZBPKMsxKT1WxTCHBYrCU7kS7hfAku4DcJ0jqOyL+jvjwQw=="
}
```
    
### Truffle version

```
"truffle-hdwallet-provider": {
   "version": "1.0.17",
   "resolved": "https://registry.npmjs.org/truffle-hdwallet-provider/-/truffle-hdwallet-provider-1.0.17.tgz",
   "integrity": "sha512-s6DvSP83jiIAc6TUcpr7Uqnja1+sLGJ8og3X7n41vfyC4OCaKmBtXL5HOHf+SsU3iblOvnbFDgmN6Y1VBL/fsg==",
   "requires": {
      "any-promise": "^1.3.0",
      "bindings": "^1.3.1",
      "web3": "1.2.1",
      "websocket": "^1.0.28"
   }
}
```

### Deploy to rinkeby testnet
```
   Deploying 'StarNotary'
   ----------------------
   > transaction hash:    0x6f040b626169431b31c014190ffbe70165e86c535d7404e9696c4e35f78ef808
   > Blocks: 1            Seconds: 13
   > contract address:    0xB4CFe8eE04CbA3e729d93B70c87aeFA0bc2be8fd
   > block number:        8592902
   > block timestamp:     1621128900
   > account:             0x081D87c859354f5b81dB20730Cf190A78c688083
   > balance:             18.747277
   > gas used:            2256305 (0x226db1)
   > gas price:           10 gwei
   > value sent:          0 ETH
   > total cost:          0.02256305 ETH
```


**PROJECT: Decentralized Star Notary Service Project** - For this project, you will create a DApp by adding functionality with your smart contract and deploy it on the public testnet.

### ToDo
This Starter Code has already implemented the functionalities you implemented in the StarNotary (Version 2) exercise, and have comments in all the files you need to implement your tasks.



### Dependencies
For this project, you will need to have:
1. **Node and NPM** installed - NPM is distributed with [Node.js](https://www.npmjs.com/get-npm)
```bash
# Check Node version
node -v
# Check NPM version
npm -v
```


2. **Truffle v5.X.X** - A development framework for Ethereum. 
```bash
# Unsinstall any previous version
npm uninstall -g truffle
# Install
npm install -g truffle
# Specify a particular version
npm install -g truffle@5.0.2
# Verify the version
truffle version
```


2. **Metamask: 5.3.1** - If you need to update Metamask just delete your Metamask extension and install it again.


3. [Ganache](https://www.trufflesuite.com/ganache) - Make sure that your Ganache and Truffle configuration file have the same port.


4. **Other mandatory packages**:
```bash
cd app
# install packages
npm install --save  openzeppelin-solidity@2.3
npm install --save  truffle-hdwallet-provider@1.0.17
npm install webpack-dev-server -g
npm install web3
```


### Run the application
1. Clean the frontend 
```bash
cd app
# Remove the node_modules  
# remove packages
rm -rf node_modules
# clean cache
npm cache clean
rm package-lock.json
# initialize npm (you can accept defaults)
npm init
# install all modules listed as dependencies in package.json
npm install
```


2. Start Truffle by running
```bash
# For starting the development console
truffle develop
# truffle console

# For compiling the contract, inside the development console, run:
compile

# For migrating the contract to the locally running Ethereum network, inside the development console
migrate --reset

# For running unit tests the contract, inside the development console, run:
test
```

3. Frontend - Once you are ready to start your frontend, run the following from the app folder:
```bash
cd app
npm run dev
```

---

### Important
When you will add a new Rinkeyby Test Network in your Metamask client, you will have to provide:

| Network Name | New RPC URL | Chain ID |
|---|---|---|
|Private Network 1|`http://127.0.0.1:9545/`|1337 |

The chain ID above can be fetched by:
```bash
cd app
node index.js
```

## Troubleshoot
#### Error 1 
```
'webpack-dev-server' is not recognized as an internal or external command
```
**Solution:**
- Delete the node_modules folder, the one within the /app folder
- Execute `npm install` command from the /app folder

After a long install, everything will work just fine!


#### Error 2
```
ParserError: Source file requires different compiler version. 
Error: Truffle is currently using solc 0.5.16, but one or more of your contracts specify "pragma solidity >=0.X.X <0.X.X".
```
**Solution:** In such a case, ensure the following in `truffle-config.js`:
```js
// Configure your compilers  
compilers: {    
  solc: {      
    version: "0.5.16", // <- Use this        
    // docker: true,
    // ...
```

## Raise a PR or report an Issue
1. Feel free to raise a [Pull Request](https://github.com/udacity/nd1309-p2-Decentralized-Star-Notary-Service-Starter-Code/pulls) if you find a bug/scope of improvement in the current repository. 

2. If you have suggestions or facing issues, you can log in issue. 

---

Do not use the [Old depreacted zipped starter code](https://s3.amazonaws.com/video.udacity-data.com/topher/2019/January/5c51c4c0_project-5-starter-code/project-5-starter-code.zip)
