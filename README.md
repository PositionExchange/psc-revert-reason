# psc-revert-reason

> Get the revert reason from a tx hash on POSIChain

[![License](http://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/authereum/eth-revert-reason/master/LICENSE)
[![NPM version](https://badge.fury.io/js/eth-revert-reason.svg)](http://badge.fury.io/js/eth-revert-reason)

## Install

```bash
 yarn add 'PositionExnchange/psc-revert-reason' --global
```

## Getting started

```bash
npx psc-revert-reason [tx_hash]
# Specific network
npx psc-revert-reason [tx_hash] [psc_testnet|psc_mainnet]

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
