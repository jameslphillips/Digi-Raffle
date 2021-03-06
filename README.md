# Digi-Raffle

Provably fair raffle on the Digibyte blockchain

Simple proof of concept code to run a provably fair raffle on the Digibyte blockchain.
This is how it works:
1. Publish a Digibyte address where Digibytes will be sent to participate in the raffle.
2. Define how many satoshis one ticket costs.
3. Publish block height of block that will be found in the future.
4. Make sure users are aware that they must prove ownership of the address they participate from in case they win.

After block X is mined we use its hash as a random value to choose the winning address.

Anyone can download this source code and verify that indeed this is the winning address. Choosing a block in the
future serves as a provable source of randomness.

How to run:

nodejs raffle.js `<Digibyte-address> <block-height> <satoshis-per-ticket>`

You'll need nodejs and npm to run. This version uses https://digiexplorer.info/ API to get blockchain information.

To run:

Clone this repository
run "npm install" inside the repo directory
