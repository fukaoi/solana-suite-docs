First, we create an on-chain "space" to store cNFTs.

{% hint style="warning" %} Once the space is created initially, it can be
utilized until the storage capacity of the space is full. {% endhint %}


### example

```ts
import { CompressedNft } from "@solana-suite/compressed-nft";

const inst = await CompressedNft.createSpace(
  "7tm6RBvnYNUb4N6Pvkc4JMk1AZX...", // secret key of the space owner
  10000,                            // space size
);

await inst.submit();
```
---

{% hint style="info" %} space size: 
The available space sizes are: `8`, `16,000`, `1,00,000`, `16,700,000`, `67,000,000`, `1,000,000,000`
{% endhint %}

---

{% embed url="https://api-reference.solana-suite.org/functions/_solana_suite_compressed_nft.CompressedNft.createSpace" %}
