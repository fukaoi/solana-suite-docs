# Install

Solana Suite library can install npm, yarn, pnpm

## Modules

| Name                         | Description                              |
| ---------------------------- | ---------------------------------------- |
| @solana-suite/airdrop        | SOL faucet for devnet, testnet           |
| @solana-suite/config         | Configuration tool                       |
| @solana-suite/compressed-nft | cNFT mint, find, transfer, gas-less      |
| @solana-suite/memo           | add Memo in SPL-TOKEN, find memo         |
| @solana-suite/multisig       | SOL, SPL-TOKEN multisig module           |
| @solana-suite/phantom        | Phantom API                              |
| @solana-suite/regular-nft    | NFT mint, find, transfer, gas-less       |
| @solana-suite/sol-native     | SOL find, transfer, gas-less             |
| @solana-suite/storage        | Decentrized storage: nft.storage, Arweave|
| @solana-suite/spl-token      | SPL-TOKEN mint, find, transfer, gas-less |

## How to install

Replace {Module Name} with the name of the module you want to use from the list
above.

{% tabs %}

{% tab title="npm" %}

```shell
npm i {Module Name}
```

{% endtab %}

{% tab title="yarn" %}

```shell
yarn add {Module Name}
```

{% endtab %}

{% tab title="pnpm" %}

```shell
pnpm add {Module Name}
```

{% endtab %}

{% endtabs %}

### exmple

```shell
// use SPL-TOKEN

npm i @solana-suite/spl-token
```
