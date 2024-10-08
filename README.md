# Storm Jetton

Jetton forked from https://github.com/OpenBuilders/notcoin-contract with no additional functionality.

# Local Development

## Install Dependencies

`npm install`

## Compile Contracts

`npm run build`

## Run Tests

`npm run test`

### Deploy or run another script

`npx blueprint run` or `yarn blueprint run`

use Toncenter API:

`npx blueprint run --custom https://testnet.toncenter.com/api/v2/ --custom-version v2 --custom-type testnet --custom-key <API_KEY> `

API_KEY can be obtained on https://toncenter.com or https://testnet.toncenter.com

## Notes

- The jetton-wallet contract does not include functionality that allows the owner to withdraw Toncoin funds from jetton-wallet Toncoin balance.

- The contract prices gas based on the *current* blockchain configuration. 
   It is worth keeping in mind the situation when the configuration has changed at the moment when the message goes from one jetton-wallet to another.
   Reducing fees in a blockchain configuration does not require additional actions.
   However, increasing fees in a blockchain configuration requires preliminary preparation - e.g. wallets and services must start sending Toncoins for gas in advance based on future parameters.

