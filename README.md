# nft_ftm_app
This repo is forked version of https://github.com/fakenickels/fantom-kittens

# How to use this repo and start the application and general notes about this project tools
1. git clone https://github.com/iambuoyant/nft_ftm_app.git

2. In the root directory of this repo run command "npm i"

3. How to setup Meta mask extention for the project on testnet: https://docs.fantom.foundation/tutorials/set-up-metamask-testnet

4. Once you setup you metamask for Fantom Test Net it going to depost 10FTM to your metamask account. You can requets more test FTM to you account by using this URL https://faucet.fantom.network/

5. You can view transactions regarding any metamask account or any smartcontract using the public address for testing FTM on this URL https://testnet.ftmscan.com/

6. Add variables WALLET_PK & PUBLIC_KEY to .env.local, .env.production & .env.staging files

7. Add PUBLIC_KEY directly to FantomKittens.sol file located in contracts directory
address payable public depositAddress = payable(add_your_metamask_public_key_here);

8. Run npm command "npm run eth:deploy-testnet" - this will deploy your contract to fantom test blockchain and console output woll be similar to below if smartcontract is succefully deployed


└─$ npm run eth:deploy-testnet

> fantom-kittens@0.1.0 eth:deploy-testnet /home/eforte/projects/blockchain/demo/nft_ftm_app
> hardhat run scripts/deploy.js --network testnet

✔ Help us improve Hardhat with anonymous crash reports & basic usage data? (Y/n) · false

Downloading compiler 0.8.4
Compiling 15 files with 0.8.4
Compilation finished successfully
Deploying contracts with the account: 0x845E1A49B4d563dDE5BC3983d0006B5cd05BC317
Account balance: 9991939979985370000
Deployed to: 0x92c2F0E4939DD8102118b37E5BB4F219576dE131

9. Add Deployed to: value from above console result to your .env.local, .env.production & .env.staging files variable "NEXT_PUBLIC_CONTRACT_ADDRESS".

10. Run npm command "npm run build " - this will add required buld files to the project to start the application

11. Run npm command "npm run start " - To start nextjs application once when console output is below

ready - started server on 0.0.0.0:3000, url: http://localhost:3000
info  - Loaded env from /home/eforte/projects/blockchain/demo/nft_ftm_app/.env.local
info  - Loaded env from /home/eforte/projects/blockchain/demo/nft_ftm_app/.env.production

12. Open the browser where you have metamask extention installed and configured and open url http://localhost:3000

13. When the app loads click on connect to wallet - this will connect your metamask account to the app to be used for minting ntfs


# Project Dependencies 
Node Ver.12.22.1