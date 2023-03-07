# Smart Contract Tests

This repository contains multiple small projects for testing smart contract interoperability



# Eth-BSC-Bridge

this deploys contracts on both ethereum and bsc and tests the bridge between them

to first set up blockchains on your local machine, run
setup up bsc chain : ganache -f https://bsc-dataseed.binance.org -p 8545
set up ethereum chain : ganache -p 7545   

use node v 18 (nvm use 18.12.0) 

make sure you have truffle installed (npm install -g truffle)
make sure truffle-config.js is set up correctly, check network names and ports
run migrations on both chains (truffle migrate --network bsc/eth)

start the bridge (written in python BRIDGE.py)

run tranfer script: truffle exec scripts/eth-bsc-transfer.js --network eth