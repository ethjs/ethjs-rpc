# User Guide

All information for developers using `ethjs-rpc` should consult this document.

## Install

```
npm install --save ethjs-rpc
```

## Usage

```js
const HttpProvider = require('ethjs-provider-http');
const EthRPC = require('ethjs-rpc');
const eth = new EthRPC(new HttpProvider('http://localhost:8545'));

eth.sendAsync({ method: 'eth_accounts' }, (err, accounts1) => {
  // null ['0x...', '0x....']
});

eth.sendAsync({ method: 'eth_gasPrice' }, (err, gasPrice) => {
  // null '0xe83922'
});
```

## Async Only

All methods are `async` only.

## Error handling

Error handling is done through function callbacks or promised catches.

## Supported Methods

`ethjs-rpc` supports all Ethereum spec RPC methods.

* [eth_protocolVersion](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_protocolversion)
* [eth_syncing](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_syncing)
* [eth_coinbase](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_coinbase)
* [eth_mining](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_mining)
* [eth_hashrate](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_hashrate)
* [eth_gasPrice](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_gasprice)
* [eth_accounts](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_accounts)
* [eth_blockNumber](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_blocknumber)
* [eth_getBalance](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_getbalance)
* [eth_getStorageAt](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_getstorageat)
* [eth_getTransactionCount](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_gettransactioncount)
* [eth_getBlockTransactionCountByHash](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_getblocktransactioncountbyhash)
* [eth_getBlockTransactionCountByNumber](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_getblocktransactioncountbynumber)
* [eth_getUncleCountByBlockHash](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_getunclecountbyblockhash)
* [eth_getUncleCountByBlockNumber](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_getunclecountbyblocknumber)
* [eth_getCode](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_getcode)
* [eth_sign](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_sign)
* [eth_sendTransaction](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_sendtransaction)
* [eth_sendRawTransaction](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_sendrawtransaction)
* [eth_call](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_call)
* [eth_estimateGas](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_estimategas)
* [eth_getBlockByHash](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_getblockbyhash)
* [eth_getBlockByNumber](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_getblockbynumber)
* [eth_getTransactionByHash](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_gettransactionbyhash)
* [eth_getTransactionByBlockHashAndIndex](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_gettransactionbyblockhashandindex)
* [eth_getTransactionByBlockNumberAndIndex](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_gettransactionbyblocknumberandindex)
* [eth_getTransactionReceipt](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_gettransactionreceipt)
* [eth_getUncleByBlockHashAndIndex](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_getunclebyblockhashandindex)
* [eth_getUncleByBlockNumberAndIndex](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_getunclebyblocknumberandindex)
* [eth_getCompilers](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_getcompilers)
* [eth_compileLLL](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_compilelll)
* [eth_compileSolidity](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_compilesolidity)
* [eth_compileSerpent](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_compileserpent)
* [eth_newFilter](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_newfilter)
* [eth_newBlockFilter](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_newblockfilter)
* [eth_newPendingTransactionFilter](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_newpendingtransactionfilter)
* [eth_uninstallFilter](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_uninstallfilter)
* [eth_getFilterChanges](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_getfilterchanges)
* [eth_getFilterLogs](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_getfilterlogs)
* [eth_getLogs](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_getlogs)
* [eth_getWork](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_getwork)
* [eth_submitWork](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_submitwork)
* [eth_submitHashrate](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_submithashrate)

* [web3_clientVersion](https://github.com/ethereum/wiki/wiki/JSON-RPC#web3_clientversion)
* [web3_sha3](https://github.com/ethereum/wiki/wiki/JSON-RPC#web3_sha3)

* [net_version](https://github.com/ethereum/wiki/wiki/JSON-RPC#net_version)
* [net_peerCount](https://github.com/ethereum/wiki/wiki/JSON-RPC#net_peercount)
* [net_listening](https://github.com/ethereum/wiki/wiki/JSON-RPC#net_listening)

* [db_putString](https://github.com/ethereum/wiki/wiki/JSON-RPC#db_putstring)
* [db_getString](https://github.com/ethereum/wiki/wiki/JSON-RPC#db_getstring)
* [db_putHex](https://github.com/ethereum/wiki/wiki/JSON-RPC#db_puthex)
* [db_getHex](https://github.com/ethereum/wiki/wiki/JSON-RPC#db_gethex)

* [shh_post](https://github.com/ethereum/wiki/wiki/JSON-RPC#shh_post)
* [shh_version](https://github.com/ethereum/wiki/wiki/JSON-RPC#shh_version)
* [shh_newIdentity](https://github.com/ethereum/wiki/wiki/JSON-RPC#shh_newidentity)
* [shh_hasIdentity](https://github.com/ethereum/wiki/wiki/JSON-RPC#shh_hasidentity)
* [shh_newGroup](https://github.com/ethereum/wiki/wiki/JSON-RPC#shh_newgroup)
* [shh_addToGroup](https://github.com/ethereum/wiki/wiki/JSON-RPC#shh_addtogroup)
* [shh_newFilter](https://github.com/ethereum/wiki/wiki/JSON-RPC#shh_newfilter)
* [shh_uninstallFilter](https://github.com/ethereum/wiki/wiki/JSON-RPC#shh_uninstallfilter)
* [shh_getFilterChanges](https://github.com/ethereum/wiki/wiki/JSON-RPC#shh_getfilterchanges)
* [shh_getMessages](https://github.com/ethereum/wiki/wiki/JSON-RPC#shh_getmessages)


## Browser Builds

`ethjs` provides production distributions for all of its modules that are ready for use in the browser right away. Simply include either `dist/ethjs-rpc.js` or `dist/ethjs-rpc.min.js` directly into an HTML file to start using this module. Note, an `EthRPC` object is made available globally.

```html
<script type="text/javascript" src="ethjs-rpc.min.js"></script>
<script type="text/javascript">
new EthRPC(...);
</script>
```

Note, even though `ethjs` should have transformed and polyfilled most of the requirements to run this module across most modern browsers. You may want to look at an additional polyfill for extra support.

Use a polyfill service such as `Polyfill.io` to ensure complete cross-browser support:
https://polyfill.io/

## Latest Webpack Figures

```
Version: webpack 2.1.0-beta.15
Time: 859ms
             Asset    Size  Chunks             Chunk Names
    ethjs-rpc.js  175 kB       0  [emitted]  main
ethjs-rpc.js.map  219 kB       0  [emitted]  main
   [4] ./lib/index.js 5.02 kB {0} [built]
    + 13 hidden modules

Version: webpack 2.1.0-beta.15
Time: 2699ms
             Asset     Size  Chunks             Chunk Names
ethjs-rpc.min.js  78.5 kB       0  [emitted]  main
   [4] ./lib/index.js 5.02 kB {0} [built]
    + 13 hidden modules
```

## Other Awesome Modules, Tools and Frameworks

### Foundation
 - [web3.js](https://github.com/ethereum/web3.js) -- the original Ethereum JS swiss army knife **Ethereum Foundation**
 - [ethereumjs](https://github.com/ethereumjs) -- critical ethereum javascript infrastructure **Ethereum Foundation**
 - [browser-solidity](https://ethereum.github.io/browser-solidity) -- an in browser Solidity IDE **Ethereum Foundation**

### Nodes
  - [geth](https://github.com/ethereum/go-ethereum) Go-Ethereum
  - [parity](https://github.com/ethcore/parity) Rust-Ethereum build in Rust
  - [testrpc](https://github.com/ethereumjs/testrpc) Testing Node (ethereumjs-vm)

### Testing
 - [wafr](https://github.com/silentcicero/wafr) -- a super simple Solidity testing framework
 - [truffle](https://github.com/ConsenSys/truffle) -- a solidity/js dApp framework
 - [embark](https://github.com/iurimatias/embark-framework) -- a solidity/js dApp framework
 - [dapple](https://github.com/nexusdev/dapple) -- a solidity dApp framework
 - [chaitherium](https://github.com/SafeMarket/chaithereum) -- a JS web3 unit testing framework
 - [contest](https://github.com/DigixGlobal/contest) -- a JS testing framework for contracts

### Wallets
 - [ethers-wallet](https://github.com/ethers-io/ethers-wallet) -- an amazingly small Ethereum wallet
 - [metamask](https://metamask.io/) -- turns your browser into an Ethereum enabled browser =D

## Our Relationship with Ethereum & EthereumJS

 We would like to mention that we are not in any way affiliated with the Ethereum Foundation or `ethereumjs`. However, we love the work they do and work with them often to make Ethereum great! Our aim is to support the Ethereum ecosystem with a policy of diversity, modularity, simplicity, transparency, clarity, optimization and extensibility.

 Many of our modules use code from `web3.js` and the `ethereumjs-` repositories. We thank the authors where we can in the relevant repositories. We use their code carefully, and make sure all test coverage is ported over and where possible, expanded on.
