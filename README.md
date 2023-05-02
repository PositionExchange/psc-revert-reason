# eth-revert-reason

> Get the revert reason from a tx hash on Ethereum

[![License](http://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/authereum/eth-revert-reason/master/LICENSE)
[![NPM version](https://badge.fury.io/js/eth-revert-reason.svg)](http://badge.fury.io/js/eth-revert-reason)

## Install

```bash
 yarn add 'qtnx/eth-revert-reason' --global
```

## Notes
1. For now, this works consistently with the [Infura](https://infura.io/) and [Alchemy](https://docs.alchemyapi.io/) providers. Any other providers that you pass in may not work.
2. There are rare cases where a revert reason may be 'x' from the context of one block but it will be 'y' from the context of another block. This may cause inconsistencies.
3. This package relies on the ethers.js default provider. This provider may be subject to rate limits or inconsistencies. For consistent results, please pass in your own provider.
4. Alchemy's provider v2 uses Geth.


## Getting started

```bash
npx eth-revert-reason [tx_hash]
# Specific network
npx eth-revert-reason [tx_hash] [psc_testnet|psc_mainnet]

```

## Future work
The following features will be added over time:

1. A better way to determine whether or not a node is full-archive.
2. A better way to determine whether or not a node exposes Parity `trace` methods.
3. Reduce the number of calls made by the provider.
4. Use raw RPC calls instead of a library
    - Will require unwrapping the provider from the library if provider is still a parameter
        - Note: this would still require using the ethers default provider


## Test

```bash
npm test
```

## License

[MIT](LICENSE)
