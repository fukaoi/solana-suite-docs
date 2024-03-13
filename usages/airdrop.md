`@solana-suite/airdrop`

It is used to faucet SOL required for development on devnet and testnet, but not
on mainnet.

### example

```ts

import { Airdrop } from "@solana-suite/airdrop";

await Airdrop.request(
    "4nfN9iymjRaYBpiy1j..."  // Wallet address
);

```

{% embed url="https://api-reference.solana-suite.org/functions/_solana_suite_airdrop.Airdrop.request" %}
