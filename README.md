# Parity Multisig Library Self-Destruct — PoC

> **Educational Purpose Only** — This PoC is created for security research and education
> purposes only. It runs against a fork, not mainnet.

## Quick Start

```bash
git clone https://github.com/NomosLabs-Security/poc-parity-multisig-2017
cd poc-parity-multisig-2017
forge test -vvvv
```

## Details

- **Exploit Date:** 2017-11-06
- **Fork Block:** #4501968 (one block prior)
- **Expected Output:** Library contract self-destructed, dependent wallets lose functionality
- **Full Analysis:** [NomosLabs Security Intelligence Archive](https://nomoslabs.io/archive/parity-multisig-2017)

## Description

This PoC demonstrates:
1. The library contract was in an uninitialized state
2. Anyone could call initWallet() to become the owner
3. The owner could call kill() to trigger selfdestruct
4. Dependent proxy wallets lose all functionality

## RPC Providers

```
Alchemy:   https://eth-mainnet.alchemyapi.io/v2/YOUR_KEY
Infura:    https://mainnet.infura.io/v3/YOUR_KEY
QuickNode: https://YOUR_ENDPOINT.quiknode.pro/YOUR_KEY
```

## License

MIT — For educational use only.
