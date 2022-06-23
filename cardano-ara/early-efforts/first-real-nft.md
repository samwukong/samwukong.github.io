# First Real NFT

The first real batch of NFTs that I made were selected from mathematically generated images that I had already created with a python program of mine. I say real test, because I did generate a single NFT first a while back, but it was of poor quality. Although it did expose me to the process.&#x20;

I selected three images for this test and built metadata JSON files for them. Overall, again, the process was fairly simple with no real surprises. All of this was handled in the terminal, and there were only some areas where I had to research alternative methods for what I was trying to do with the NFT minting process.

I found the NFT metadata template standards found in [CIP-25](https://cips.cardano.org/cips/cip25/) to be helpful and generally used them as a standard. I didn't included the declaration of Version 1.0 and so far this doesn't seem to have made a difference. I suppose with the Vasil HF and future CIPs amending or adding to metadata this might be more important. And if for nothing other than completeness in the JSON file I might add it.

NFT Names: Rough NFT 1, 2, 3

Minted in this transaction: 3

Policy: Locked after 10,000 slots from the minting transaction

The errors that I made here are:

1. I did not properly scrub the metadata file I used for my first super early test and technically wound up with the NFT name of "Tiger". This was not intended.
2. I foolishly tried to add all three metadata files to the transaction under the impression that the blockchain would be able to determine which asset name corresponded to which JSON file. This was inaccurate and I have learned from my mistake (more in the second NFT minting). Instead, all three NFTs possess only the first metadata from the Rough NFT 1.

```
{ 1146f07a9777f5ca323ce2bc478f733721d15804573ff91291c247ab: { 
Tiger: { 
id: "1", 
name: "Rought NFT 1", 
image: "ipfs://QmfD12nQq4Q5vx3cBA1jXDimikCvVNZn2Aro8UbfgUwgzH", 
description: "Rough NFT 1" 
    } 
  } 
}
```

The transaction fee for minting three NFTs was 0.18 ₳ (or approximately 9 cents at the time of transaction), so minting multiple NFTs together can considerably reduce your per-NFT costs.

Not to undersell my lesson here, I did gain both confidence and understanding of the NFT minting process. There were a few snags with building the transaction and getting the elements correct, but ultimately I was able to submit the minting transaction just fine and the blockchain accepted it. Go Tigers!

#### Proof of Minting

The transaction hash for minting is:

[1146f07a9777f5ca323ce2bc478f733721d15804573ff91291c247ab](https://testnet.cardanoscan.io/tokenPolicy/1146f07a9777f5ca323ce2bc478f733721d15804573ff91291c247ab)
