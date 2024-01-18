`@solana-suite/compressed-nft`

Compared to traditional NFTs, cNFTs have a different method of data storage. In
regular NFTs, most of the metadata is stored on-chain. However, due to the
expensive storage fees on Solana, cNFTs adopt an off-chain storage approach.
When storing off-chain, the hash value is saved in an on-chain Merkle tree,
significantly reducing costs. This approach also improves searchability.

{% embed
url="https://api-reference.solana-suite.org/modules/_solana_suite_compressed_nft.CompressedNft"
%}

## Functions

- [Modules](modules/)
- [Mint the cNFT](./mint.md)
- [Find cNFT, Collection](./find.md)
- [Mint a collection](./mint-collection.md)
- [Transfer cNFT](./transfer.md)

