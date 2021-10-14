## Install truffle from snaps
`sudo dnf install snapd`   
`sudo ln -s /var/lib/snapd/snap /snap`   
`sudo snap install truffle --beta`   

or from npm
```npm install -g truffle```

## The project was initialized by truffle:
```truffle unbox react```   
or    
```truffle init (with no smart contract)```  

# truffle unit test
```
truffle test ./test/TestSimpleStorage.sol
truffle test ./test/simplestorage.js 
```


# Compile the smart contracts:
```truffle compile```


## create local blockchain using truffle:
To deploy our smart contracts, we're going to need to connect to a blockchain. Truffle has a built-in personal blockchain that can be used for testing. This blockchain is local to your system and does not interact with the main Ethereum network.

You can create this blockchain and interact with it using Truffle Develop.
```truffle develop```

On the Truffle Develop prompt, Truffle commands can be run by omitting the truffle prefix. For example, to run truffle compile on the prompt, type compile. The command to deploy your compiled contracts to the blockchain is truffle migrate, so at the prompt, type:

## Deploy:
```migrate```

## Deploy contracts using truffle unsing config:
```truffle migrate --reset --network develop```



# Install hardhat
npm install --save-dev hardhat   
npm install --save-dev @nomiclabs/hardhat-waffle ethereum-waffle chai @nomiclabs/hardhat-ethers ethers   

-------------------------------------------

## Run local chain from hardhat:
npx hardhat node



# Install brownie 

## requirements
nodejs
python 
python -m pip install --user pipx 
python -m pipx ensurepath 
apt-get install python3-venv 
pipx install eth-brownie

## Install solc 
sudo snap install solc 

## Add network to brownie 
brownie networks add Ethereum rinkeby_test host='https://speedy-nodes-nyc.moralis.io/e2bfe6d43f897c5ef0455cdc/eth/rinkeby' name="Eth Rinkeby Moralis" chainid=4 explorer='https://api-rinkeby.etherscan.io/api'

## Add new account to brownie
brownie accounts list brownie account new (then enter private key)

## Install Smart contract dependencies using brownie
brownie pm install smartcontractkit/chainlink-brownie-contracts@1.0.2 
brownie pm install list

## Connect to a network
brownie console --network rinkeby_test

## import account from rinkeby test network that was added
account = accounts.load("rinkeby_account")

## Deploy contract from imported account
Price_ETH.deploy({'from': account})

## call contacrt function from brownie environment Interactive console
Price_ETH[0].getThePrice()/10**8# truffle_metacoin
