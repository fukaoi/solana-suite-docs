## Mint the cNFT

To mint cNFTs, you need to first create a Space and mint collection. Please
store the addresses of the Space and mint collection in an RDB or Config file.

### example

[Full example code](https://github.com/fukaoi/solana-suite/blob/main/examples/integration11-compressed-nft.ts)

basic usage

```ts
import { CompressedNft } from "@solana-suite/compressed-nft";

const inst = await CompressedNft.mint(
  owner.secret,
  {
    filePath: "./lion.png", // Upload image path or uri
    name: "Lion ",          // mint name
    symbol: "LION",         // mint symbole
    royalty: 20,            // royalty percentage
  },
  "space address",          // space address
  "collection address",     // collection address
);

await inst.submit();
```
{% hint style="info" %} 
`filePath` or `uri`: 
You can specify a URI in addition to a filePath. The URI allows you to specify the URL of already uploaded content, such as images or videos.
When you specify a filePath, the content upload is handled in the background, which means that the time for minting to complete may vary depending on the size of the content.
{% endhint %}


---

{% embed url="https://api-reference.solana-suite.org/functions/_solana_suite_compressed_nft.CompressedNft.mint" %}
