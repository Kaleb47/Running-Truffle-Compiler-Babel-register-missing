# Running-Truffle-Compiler-Babel-register-missing
After deleting and reinstalling the npm package, @babel-register is still missing



First, I fixed my truffle-config.js file 


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
