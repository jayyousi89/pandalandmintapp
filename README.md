# Welcome to panda land NFTs đ

![](https://github.com/jayyousi89/pandalandmintapp/blob/main/logo-blob.png)

All the code in these repos was created and explained by HashLips on the main YouTube channel.

To find out more please visit:

[đē Discord](https://discord.gg/3CpugxCBa4)

[đŦ Telegram](https://t.me/nftsland)

[đĻ Twitter](https://twitter.com/pandalandnfts)

[âšī¸ Website](https://pandalandnfts.com)

# panda land NFTs minting dapp đĨ

This repo provides a nice and easy way for linking an existing NFT smart contract to this minting dapp. There are two ways of using this repo, you can go the simple route or the more complex one.

The simple route is so simple, all you need to do is download the build folder on the release page and change the configuration to fit your needs. (Follow the video for a walk through).

The more complex route allows you to add additional functionality if you are comfortable with coding in react.js. (Follow the below instructions for a walk through).

## Installation đ ī¸

If you are cloning the project then run this first, otherwise you can download the source code on the release page and skip this step.

```sh
git clone https://github.com/The-Stripes-NFT/nft-minting-app.git
```

Make sure you have node.js installed so you can use npm, then run:

```sh
npm install
```

## Usage âšī¸

In order to make use of this dapp, all you need to do is change the configurations to point to your smart contract as well as update the images and theme file.

For the most part all the changes will be in the `public` folder.

To link up your existing smart contract, go to the `public/config/config.json` file and update the following fields to fit your smart contract, network and marketplace details. The cost field should be in wei.

Note: this dapp is designed to work with the intended NFT smart contract, that only takes one parameter in the mint function "mintAmount". But you can change that in the App.js file if you need to use a smart contract that takes 2 params.

```json
{
  "CONTRACT_ADDRESS": "0xB6847E80Fb7fd2253B688629C37870055A1246c7",
  "SCAN_LINK": "https://polygonscan.com/token/0xB6847E80Fb7fd2253B688629C37870055A1246c7",
  "NETWORK": {
    "NAME": "Polygon",
    "SYMBOL": "Matic",
    "ID": 137
  },
  "NFT_NAME": "Baby Panda NFT",
  "SYMBOL": "BPN",
  "MAX_SUPPLY": 500,
  "WEI_COST": 6000000000000000000,
  "GAS_LIMIT": 285000,
  "DISPLAY_COST": 6,
  "MARKETPLACE": "Opeansea",
  "MARKETPLACE_LINK": "https://opensea.io/collection/baby-panda-nfts",
  "WEBSITE_LINK": "https://pandalandnfts.com",
  "SHOW_BACKGROUND": true
}
```

Make sure you copy the contract ABI from remix and paste it in the `public/config/abi.json` file.
(follow the youtube video if you struggle with this part).

Now you will need to create and change 2 images and a gif in the `public/config/images` folder, `bg.gif`, `example.gif` and `logo.gif`.

Next change the theme colors to your liking in the `public/config/theme.css` file.

```css
:root {
  --primary: #ebc908;
  --primary-text: #1a1a1a;
  --secondary: #ff1dec;
  --secondary-text: #ffffff;
  --accent: #ffffff;
  --accent-text: #000000;
}
```

Now you will need to create and change the `public/favicon.ico`, `public/logo192.gif`, and
`public/logo512.gif` to your brand images.

Remember to update the title and description the `public/index.html` file

```html
<title>The panda land NFTs</title>
<meta name="description" content="Mint your Baby panda NFT" />
```

Also remember to update the short_name and name fields in the `public/manifest.json` file

```json
{
  "short_name": "BPN",
  "name": "Baby Panda NFT"
}
```

After all the changes you can run.

```sh
npm run start
```

Or create the build if you are ready to deploy.

```sh
npm run build
```

Now you can host the contents of the build folder on a server.

That's it! you're done.
