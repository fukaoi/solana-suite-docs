`@solana-suite/storage`

We upload content to decentralized file storage systems such as Arweave and
nft.storage.

### example

[Full example code](https://github.com/fukaoi/solana-suite/blob/main/examples/integration13-upload-content.ts)

upload content file(e.g: image, movie,,,) in nftStorage

```ts
import { Storage } from "@solana-suite/storage";

await Storage.uploadFile(
    "file path",  // upload content file path in local path  
    "nftStorage"  // set storage type
);
```

upload content file(e.g: image, movie,,,) in arweave

```ts
import { Storage } from "@solana-suite/storage";

await Storage.uploadFile(
    "./animals.jpeg",                     // upload content file path in local path  
    "arweave",                            // set storage type
    {feePayer: "HTpCqDfm7NwxKrwaQww..."}  // fee payer,s secret
);
```
{% hint style="warnning" %} 
Arweave is a paid service, so specifying the fee payer is always necessary.
{% endhint %}


upload nft metadata(json) in nft.storage 

```ts
import { Storage } from "@solana-suite/storage";

const meta = {
    name: "Tiger",                    // NFT's name in offchain   
    symbol: "TIGER",                  // NFT's symbol in offchain 
    description: "tiger description", // optional field 
    image: "https://......",          // Uploaded image url 
};

const res = await Storage.uploadData(meta, "nftStorage");
```

upload nft metadata(json) in arweave

```ts
import { Storage } from "@solana-suite/storage";

const meta = {
    name: "Tiger",    // NFT's name in offchain   
    symbol: "TIGER",  // NFT's symbol in offchain 
    description: "This nft is tiger content", // optional field 
    image: "https://......", // Uploaded image url 
};

const res = await Storage.uploadData(
    meta, 
    "arweave", 
    {feePayer: "HTpCqDfm7NwxKrwaQww..."} // fee payer,s secret 
);
```
---

{% embed url="https://api-reference.solana-suite.org/modules/_solana_suite_storage.Storage" %}
