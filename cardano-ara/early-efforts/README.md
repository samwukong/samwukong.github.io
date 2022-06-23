---
description: Early efforts while working in cardano-cli
---

# Early Efforts

![](<../../.gitbook/assets/image (1).png>)

Working in the terminal on Linux and macOS is comfortable enough for me. I've spent time focused on learning the general structure of commands, reading documentation, and creating scripts. Primarily this has been focused device discovery, mapping network footprints, and other efforts related to Cyber Security.

Changing focus a little bit I began learning to use cardano-cli, cardano-wallet, and other tools to perform tasks related to navigating on the Cardano blockchain. During this early phase this includes:

* Running a node
* Querying the blockchain
* Creating key pairs and addresses
* Creating full wallets
* Creating and sending single transactions
* Creating and sending multiple actions in a single transaction

However, I made an effort to understand more about working with Cardano native assets. This is initially to better understand the mechanics of them and later to be able to relate the actions required for corresponding programs built for those purposes.

Ultimately, the goal is to be able to establish, deploy, and run various projects on Cardano suitable for both recreational and enterprise use cases. The idea of enterprise NFTs and smart contracts fascinate me. I can see great future utility in how NFTs both serve as proof of ownership (for digital, real, or intellectual property) and for how they can better facilitate certain elements in business operations.&#x20;

For now, I'm simply recording my journey through the process and declaring a proof of knowledge along the way.

### [Minting a Native Token](https://app.gitbook.com/s/e0OBzf0D1zIir1P9Mico/\~/changes/4Gp6BwPpN3fLGho6NsKb/cardano-ara/early-efforts/minting-a-native-token)

Token name: ViralNinja

Amount Minted: 10 million

Minting policy: locked shortly after minting

#### Proof of Minting

The transaction hash for minting is:

[632187ebe1ad6c41dfb63c11a811a947fb84e698a03f2690aa732f783295584a](https://testnet.cardanoscan.io/transaction/632187ebe1ad6c41dfb63c11a811a947fb84e698a03f2690aa732f783295584a)

### [First Real NFT](https://app.gitbook.com/s/e0OBzf0D1zIir1P9Mico/\~/changes/4Gp6BwPpN3fLGho6NsKb/cardano-ara/early-efforts/first-real-nft)

NFT Names: Rough NFT 1, 2, 3

Minted in this transaction: 3

Policy: Locked after 10,000 slots from the minting transaction

#### Proof of Minting

The transaction hash for minting is:

[1146f07a9777f5ca323ce2bc478f733721d15804573ff91291c247ab](https://testnet.cardanoscan.io/tokenPolicy/1146f07a9777f5ca323ce2bc478f733721d15804573ff91291c247ab)

### [Second NFT Minting (with Royalty)](https://app.gitbook.com/s/e0OBzf0D1zIir1P9Mico/\~/changes/4Gp6BwPpN3fLGho6NsKb/cardano-ara/early-efforts/second-nft-minting-with-royalty)

Token Names: Rough NFT 7, 8

Number Minted: 2

Policy: Locked after 2+ million slots after the transaction (roughly 30 days)

Royalty Set: 20%

#### Proof of Minting

The transaction hash for the minting is:

[eca56a05f792154bd97bc6e9237af45340c58acec8c7520917e47101](https://testnet.cardanoscan.io/tokenPolicy/eca56a05f792154bd97bc6e9237af45340c58acec8c7520917e47101)

Additionally, the transaction information for minting and burning the royalty token is:

{% embed url="https://testnet.cardanoscan.io/token/eca56a05f792154bd97bc6e9237af45340c58acec8c7520917e47101?tab=minttransactions" %}
Rough NFT Royalty Token Minting and Burning
{% endembed %}

### Current Phase Confidence

At the conclusion of this early phase I feel confident in being about to create the most common and most used forms of digital assets (also known as native assets) on Cardano, as well as being able to process a reasonably broad range of transaction types.

I would declare my confidence high on these actions.

I would declare my confidence moderate to practiced on creating scripts and other pseudo-programs for these actions.

### Future Plans

Future plans include writing a Royalty Token pointing to a Plutus smart contract that directs the payments to two ADAhandle NFTs. I really wish this could be done just in the simple 777 standard (that is, pointing to an ADAhandle) but it doesn't appear that the blockchain will query the ADAhandle resolver on its own.&#x20;

I will build a process to listen for transactions and then execute a set action. Such as, receiving a specified amount in a transaction to a specific wallet and then returning a prescribed reward or purchase. Also, I will begin putting these concepts into a program that can be run in a server for a better automated process.
