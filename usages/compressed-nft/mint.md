## Mint the cNFT

To mint cNFTs, you need to first create a Space and mint collection. Please
store the addresses of the Space and mint collection in an RDB or Config file.

### example

* basic usage

```ts
import { CompressedNft } from "@solana-suite/compressed-nft";

const inst = await CompressedNft.mint(
  owner.secret,
  {
    filePath: "./lion.png", // Upload image path
    name: "Lion ",          // mint name
    symbol: "LION",         // mint symbole
    royalty: 20,            // royalty percentage
  },
  "space address",          // space address
  "collection address",     // collection address
);

await inst.submit();
```

[Full example code](https://github.com/fukaoi/solana-suite/blob/main/examples/integration11-compressed-nft.ts)

{% embed
url="<https://api-reference.solana-suite.org/functions/_solana_suite_compressed_nft.CompressedNft.mint>"
%}
