# Smart Contract Tests

This repository contains multiple small projects for testing smart contract interoperability

Make sure Tuffle is installed

Make sure Ganache is installed (do not use gui)

# Eth-BSC-Bridge

this deploys contracts on both ethereum and bsc and tests the bridge between them

to first set up blockchains on your local machine, you need to install ganache

setup up bsc chain : 
ganache -f https://bsc-dataseed.binance.org -p 8545

set up ethereum chain : 
ganache -p 7545   

use node v < 19 (nvm use 18.12.0) 

make sure you have truffle installed (npm install -g truffle)

make sure truffle-config.js is set up correctly, check network names and ports

set bsc priv key in bridge.py
set eth priv key in eth-bsc-transfer.js
priv key will be generated when ganache is run, use first acc. for this example
run migrations on both chains 

truffle migrate -reset --network bsc/eth

start the bridge (written in python BRIDGE.py)

run tranfer script: truffle exec scripts/eth-bsc-transfer.js --network eth
