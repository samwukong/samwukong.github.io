# Second NFT Minting (with Royalty)

After successfully (in a manner of degrees) minting the first three NFTs I then set about to set a Royalty token with the NFT policy. This is one of the key elements that I wanted to test. I read and understood the [CIP-27](https://cips.cardano.org/cips/cip27/) community standard for Royalty Tokens and wanted to put this into effect. To me, it's clear that many NFT projects will desire or require this functionality so it's an important one to get correct.

Token Names: Rough NFT 7, 8

Number Minted: 2

Policy: Locked after 2+ million slots after the transaction (roughly 30 days)

Royalty Set: 20%

Disclaimer: I realize that 20% royalty is not realistic but I did this more for the test of the token.

I will admit I had more apprehension about the concept of submitting a transaction for an "unnamed token" than I should have. But, this was my first time.

I had to do quite a bit of research to figure out how I define no name for a token with a policy ID. No real useful information or examples existed that I could find in a day, so I went with the most logical thing in my instincts.

I sent the policy ID and token name as "$PolicyID." In other words, I just left the token name literally blank. Turns out that's what you're supposed to do. So, if anyone else types a search for something like "how to build an unnamed token for royalties" in the search bar, hopefully it brings you here.

I submitted the first token with the 777 tag as in the standard and just a single address for the payout. It was accepted just fine.

```
{
   addr: "addr_test1vrv70hdddtknrzeqjhzr7jlmttplyx9562vks4ulpqqwu2gfv74k8",
   rate: "0.2"
}
```

I then immediately burned the token as recommended. This process was fairly straight forward. Essentially I just resubmit a mint transaction while the policy is still open, but I input 1 of the unnamed token and returned -1. This effectively burns the token and preserves UTxO space.

After this, I minted the two NFTs planned for this test. This time I learned from the first real multiple NFT minting process and combined the metadata JSON files appropriately.&#x20;

I learned that if multiple NFTs are being minted together a clear way to assign the correct metadata is to build it all in one JSON file. If the NFTs are minted on-demand then the JSON can be created just for that one NFT just fine.

The transaction fee for minting two NFTs was 0.18 ₳ (or approximately 9 cents at the time of transaction), again proving that minting multiple NFTs together considerably reduces costs.

#### Proof of Minting

The transaction hash for the minting is:

[eca56a05f792154bd97bc6e9237af45340c58acec8c7520917e47101](https://testnet.cardanoscan.io/tokenPolicy/eca56a05f792154bd97bc6e9237af45340c58acec8c7520917e47101)

Additionally, the transaction information for minting and burning the royalty token is:

{% embed url="https://testnet.cardanoscan.io/token/eca56a05f792154bd97bc6e9237af45340c58acec8c7520917e47101?tab=minttransactions" %}
Rough NFT Royalty Token Minting and Burning
{% endembed %}

