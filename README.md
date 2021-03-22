# Running-Truffle-Compiler-Babel-register-missing
After deleting and reinstalling the npm package, @babel-register is still missing



First, I fixed my truffle-config.js file 
here is truffle-config.js

```
require('babel-polyfill');
require('dotenv');
config();



module.exports = {
  

  networks: {
   development : {
    host : "127.0.0.1",
    port: 7545,
    netowrk_id: "*"
   },
 
  },
contracts_directory:'./src/contracts/',
contracts_build_directory: './src/abis/',
 
  
  compilers: {
    
    solc: {
      version: "0.5.0",
     optimizer: {
      enabled: true,
      runs: 200
     }
    }
  }
}
```
next I installed npm and loaded package-lock.json


```
{
  "name": "bootcamp",
  "version": "0.2.0",
  "description": "Decentralized Ethereum Token Exchange",
  "author": "dev@dappuniversity.com",
  "private": true,
  "homepage": ".",
  "engines": {
    "node": "8.11.1"
  },
  "dependencies": {
    "@truffle/hdwallet-provider": "1.1.0",
    "apexcharts": "3.6.3",
    "babel-polyfill": "6.26.0",
    "babel-preset-env": "1.7.0",
    "babel-preset-es2015": "6.24.1",
    "babel-preset-stage-2": "6.24.1",
    "babel-preset-stage-3": "6.24.1",
    "babel-register": "6.26.0",
    "bootstrap": "4.5.2",
    "chai": "4.2.0",
    "chai-as-promised": "7.1.1",
    "chai-bignumber": "3.0.0",
    "dotenv": "8.2.0",
    "lodash": "4.17.20",
    "moment": "2.29.0",
    "openzeppelin-solidity": "2.1.3",
    "react": "16.13.1",
    "react-apexcharts": "1.3.7",
    "react-bootstrap": "1.3.0",
    "react-dom": "16.13.1",
    "react-redux": "7.2.1",
    "react-scripts": "3.4.3",
    "redux": "4.0.5",
    "redux-logger": "3.0.6",
    "reselect": "4.0.0",
    "solidity-coverage": "0.7.10",
    "truffle": "5.1.45",
    "truffle-flattener": "1.5.0",
    "truffle-hdwallet-provider-privkey": "0.3.0",
    "web3": "1.2.6"
  },
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test",
    "eject": "react-scripts eject"
  },
  "eslintConfig": {
    "extends": "react-app"
  },
  "browserslist": [
    ">0.2%",
    "not dead",
    "not ie <= 11",
    "not op_mini all"
  ]
}
```


```


Then I ran truffle compile in my terminal

```
kalebamarante@KALEBS-MacBook-Pro ~ % truffle compile
Error: Cannot find module 'babel-register'
Require stack:
- /Users/kalebamarante/truffle-config.js
- /usr/local/lib/node_modules/truffle/node_modules/original-require/index.js
- /usr/local/lib/node_modules/truffle/build/cli.bundled.js
    at Function.Module._resolveFilename (node:internal/modules/cjs/loader:925:15)
    at Function.Module._load (node:internal/modules/cjs/loader:769:27)
    at Module.require (node:internal/modules/cjs/loader:997:19)
    at require (node:internal/modules/cjs/helpers:92:18)
    at Object.<anonymous> (/Users/kalebamarante/truffle-config.js:1:1)
    at Module._compile (node:internal/modules/cjs/loader:1108:14)
    at Object.Module._extensions..js (node:internal/modules/cjs/loader:1137:10)
    at Module.load (node:internal/modules/cjs/loader:973:32)
    at Function.Module._load (node:internal/modules/cjs/loader:813:14)
    at Module.require (node:internal/modules/cjs/loader:997:19)
    at Object.require (node:internal/modules/cjs/helpers:92:18)
    at Function.load (/usr/local/lib/node_modules/truffle/build/webpack:/packages/config/dist/index.js:161:1)
    at Function.detect (/usr/local/lib/node_modules/truffle/build/webpack:/packages/config/dist/index.js:150:1)
    at Object.run (/usr/local/lib/node_modules/truffle/build/webpack:/packages/core/lib/commands/compile.js:68:1)
    at Command.run (/usr/local/lib/node_modules/truffle/build/webpack:/packages/core/lib/command.js:136:1)
    at Object.<anonymous> (/usr/local/lib/node_modules/truffle/build/webpack:/packages/core/cli.js:57:1)
    at __webpack_require__ (/usr/local/lib/node_modules/truffle/build/webpack:/webpack/bootstrap:19:1)
    at /usr/local/lib/node_modules/truffle/build/webpack:/webpack/bootstrap:83:1
    at Object.<anonymous> (/usr/local/lib/node_modules/truffle/build/cli.bundled.js:89:10)
    at Module._compile (node:internal/modules/cjs/loader:1108:14)
    at Object.Module._extensions..js (node:internal/modules/cjs/loader:1137:10)
    at Module.load (node:internal/modules/cjs/loader:973:32)
    at Function.Module._load (node:internal/modules/cjs/loader:813:14)
    at Function.executeUserEntryPoint [as runMain] (node:internal/modules/run_main:76:12)
    at node:internal/main/run_main_module:17:47
Truffle v5.1.63 (core: 5.1.63)
Node v15.5.0
```


