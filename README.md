# Web3 Secret Club

## What it does

With W3SC(Web3 Secret Club), anyone can earn CryptoCoin on IPFS && Any EVM Chain on the Web3 world by selling anything.

## Links

* [Demo Video](https://www.loom.com/share/93536134f1564167a5c5c98a279614cd)
* [DApp Demo](https://secret3.nfttop.best/club/1/bafkreibehkc46yptzfje7ohyqqe2m4k3ycskm37smgjyyzg6wyklltzmw4)
* [DApp Source Code](https://github.com/NftTopBest/web3-secret-club/blob/main/web-app)
* [Contact Source Code](https://github.com/NftTopBest/web3-secret-club/blob/main/solidity-contract/Secret3.sol)
* [Contact Deployment](https://mumbai.polygonscan.com/address/0xCD8eC2f6787458C4476931623a71B97D85dAEedD)
* [All Screenshot](https://github.com/NftTopBest/web3-secret-club/blob/main/screenshot)

<img src="https://github.com/NftTopBest/web3-secret-club/raw/main/screenshot-1.png" />

## Features

* creators can manage their web3 secret clubs
  * create new club [source](https://github.com/NftTopBest/web3-secret-club/blob/main/web-app/src/components/secret3/dialog/createCategory.vue)
    * club logo (upload to IPFS)
    * basic price (for the token sell price)
    * invite commission (for club owner promote marketing)
    * all data pack into json and submit to IPFS via `NFT.Stroage` SDK [source](https://github.com/NftTopBest/web3-secret-club/blob/main/web-app/src/composables/useNFTStorage.ts)
  * add item for the Club [source](https://github.com/NftTopBest/web3-secret-club/blob/main/web-app/src/components/secret3/dialog/createItem.vue)
    * club item has banner, title, intro, item unlock minimum token number, encrypted content fields
    * all the fields get packed into an json and upload to IPFS
      * secret content get encrypted before packed into json
    * creator can also add their own NFT contract as additional decrypt condition for club member
    * currently as POC only support text content, will support many more formats for the next step: music/movie/images
* audiences can join clubs and get club secret content by mint club tokens (ERC1155 tokens provide by platform)  [source](https://github.com/NftTopBest/web3-secret-club/blob/main/web-app/src/components/secret3/items.vue)
  * follow/join club by mint at least 1 token of club NFT
  * invite friends to join club and get commission rewards
  * mint club NFT tokens
    * total pay amount = basicPrice * tokenAmount
    * inviter get ${inviteCommission}% of the payment
  * check club secret content items list
  * get decrypted content automaticly  [source](https://github.com/NftTopBest/web3-secret-club/blob/main/web-app/src/pages/secret3/club/%5BtokenId%5D/%5Bcid%5D.vue)
* platform get 1% fee for all of the token mint payments
* contract Build base on the `ERC1155` [source](https://github.com/NftTopBest/web3-secret-club/blob/main/solidity-contract/Secret3.sol)

## How it works

In web3 secret club, we have two kinds of users: creators and audiences, creator can create secret club and secret items in club,
while the audiences can follow/join club and decrypt secret items if they meet the unlock conditions.

<img src="https://github.com/NftTopBest/web3-secret-club/raw/main/1.user-action.png" />

Audiences follow/join club by mint any number of club NFT tokens(ERC1155 token provide by platform), decrypt secret item automaticly if they have enough tokens.

<img src="https://github.com/NftTopBest/web3-secret-club/raw/main/2.action-flow.png" />

A web3 secret club can be use for any kinds of creator economy relative group, media content, memberships.

* Video lessons
* Academic paper
* Drawing & Painting as ERC721 NFTs
* Fiction Books: Short stories, novellas, as NFT
* Films as NFT
* Music & Sound Design: Tracks, beats as NFT
* Photography
* Sell your Top 10 lists
* Sell your crypto tips
* Sell your keto cookbook
* Sell your new emojis
* Seriously, sell anything!

<img src="https://github.com/NftTopBest/web3-secret-club/raw/main/3.use-cases.png" />

## Application Tech Stack

* [x] IPFS
* [x] OpenZepplin
* [x] ERC1155
* [x] Hardhat
* [x] Vercel
* [x] TailwindCSS
* [x] Vue3
* [x] Pinia (state store)
* [x] PWA
* [x] Vite2

<img src="https://github.com/NftTopBest/web3-secret-club/raw/main/screenshot-2.png" />

## What's next

* Build more UI/UX for different areas/tracks users
* Marketing && Promotion for the platform
* Improve the UX/UI design
* Make a great Landing page
* Find 100 NFT KOLs to use our platform and get earned
* Help top 100 users to get earned with $1M worths of Crypto Assets
