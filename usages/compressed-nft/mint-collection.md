A Collection is a mechanism for grouping Solana NFTs.

### example

```ts
import { CompressedNft } from "@solana-suite/compressed-nft";

const inst = await CompressedNft.mintCollection(
  "HTpCqDfm7NwxKrwaQww6yHp...",  // mint collection's owner Secret  
  {
    filePath: "./animals.jpeg",  // upload image path
    name: "Animals Collection",  // collection name
    symbol: "ANIC",              // collection symbol
  }
);

await inst.submit();
```
---

{% embed url="https://api-reference.solana-suite.org/functions/_solana_suite_compressed_nft.CompressedNft.mintCollection" %}
