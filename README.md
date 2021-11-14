# Farming

truffle exec scripts/create_lp.js --network bsc_testnet
Using network 'bsc_testnet'.

Deploying contracts...
Creating liquidity...
Adding liquidity...

In frontend/src/sushi/lib/constants.js scroll to CHAIN_ID 97 (bsc_testnet)
Paste this 0xd7802ACb27Dc878e529FbeADE86486473d8857F9 LP token address into .env and supportedPools/lpAddresses
Paste this 0xb05AE26B5A4db60cd70EFA837cEB4d797A967d4F Token1 address into supportedPools/tokenAddresses
Paste this 0x22D4A7AaC4034d23F90adaa62D57A41cA98A249C Token2 address into supportedPools/tokenAddresses

Also:
 * Check latests block on https://testnet.bscscan.com/
 * Add to that number ~1000 blocks and put this number in .env START_BLOCK
 * In .env END_BLOCK add higher number than START_BLOCK (e.g. 1M higher)
 * Optionally edit also TOKENS_PER_BLOCK & ALLOCATION_POINT (More info in Masterclass video)

Once you completed steps above run:
truffle migrate --reset --network bsc_testnet




Starting migrations...
======================
> Network name:    'bsc_testnet'
> Network id:      97
> Block gas limit: 30000000 (0x1c9c380)


1_initial_migration.js
======================

   Replacing 'Migrations'
   ----------------------
   > transaction hash:    0xc0ae3093422b5e0997579a9afab7b9940ad5bb83eba06f81acdcb175da399a17
   > Blocks: 5            Seconds: 13
   > contract address:    0x518ce9e9614119B37f0bBCc798bD78b9C0cB8e9c
   > block number:        14117639
   > block timestamp:     1636926646
   > account:             0xD109fc566401ca57445810b9A3C187876cf44544
   > balance:             1.151379582297356405
   > gas used:            159195 (0x26ddb)
   > gas price:           10 gwei
   > value sent:          0 ETH
   > total cost:          0.00159195 ETH


   > Saving migration to chain.
   > Saving artifacts
   -------------------------------------
   > Total cost:          0.00159195 ETH


2_deploy.js
===========

   Deploying 'SushiToken'
   ----------------------
   > transaction hash:    0x21ad7a861b64d2dc5f6fd19e0ccd150ac6b124b1a48e98796511e6bc28c128f2
   > Blocks: 3            Seconds: 9
   > contract address:    0xCb7a3dA2dA01b092C118d38AF2af3f0ae28Abd2B
   > block number:        14117650
   > block timestamp:     1636926679
   > account:             0xD109fc566401ca57445810b9A3C187876cf44544
   > balance:             1.123984602297356405
   > gas used:            2697160 (0x2927c8)
   > gas price:           10 gwei
   > value sent:          0 ETH
   > total cost:          0.0269716 ETH


   Deploying 'MasterChef'
   ----------------------
   > transaction hash:    0x0b52222c60e5c3e2ec2fe8705bd14a09697257458923c4596f7a8824279c7366
   > Blocks: 3            Seconds: 9
   > contract address:    0xac3334F4D03E966aABC17C9751fD671f3Ebc0061
   > block number:        14117657
   > block timestamp:     1636926700
   > account:             0xD109fc566401ca57445810b9A3C187876cf44544
   > balance:             1.096583412297356405
   > gas used:            2740119 (0x29cf97)
   > gas price:           10 gwei
   > value sent:          0 ETH
   > total cost:          0.02740119 ETH

In frontend/src/sushi/lib/constants.js scroll to CHAIN_ID 4 (if deployed on Rinkeby) or CHAIN_ID 97 (if deployed on bsc_testnet)

Paste this 0xCb7a3dA2dA01b092C118d38AF2af3f0ae28Abd2B into contractAddresses/sushi

Paste this 0xac3334F4D03E966aABC17C9751fD671f3Ebc0061 into contractAddresses/masterChef

   > Saving migration to chain.
   > Saving artifacts
   -------------------------------------
   > Total cost:          0.05437279 ETH


Summary
=======
> Total deployments:   3
> Final cost:          0.05596474 ETH
