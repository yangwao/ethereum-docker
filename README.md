# ethereum-docker

ethereum docker nodes for development
if you want to touch real transactions on testnets, like privateChain (devchain) or Rinkeby and not wanna use `truffle develop` or `testrpc`

### rinkeby
incl light and full node for rinkeby

flight control

```bash
docker-compose up fullnode
```

### privateChain
bootstrap node, eth and monitoring node

```bash
docker-compose up -d
```


### handy copy pasta tricks

```bash

geth --password /root/.accountpassword account list
geth --password /root/.accountpassword account new

docker exec -it eth_fullnode_1 geth attach ipc://root/.ethereum/rinkeby/geth.ipc

```

### web3

```javascript
miner.start()
miner.stop()

personal.newAccount("password")
eth.coinbase
eth.getBalance(eth.coinbase)
personal.unlockAccount(eth.coinbase, 'password', 10000)

personal.unlockAccount('0x007ccffb7916f37f7aeef05e8096ecfbe55afc2f', '', 10000)
var sender = eth.accounts[0];var receiver = eth.accounts[1];var amount = web3.toWei(0.01, "ether")
eth.sendTransaction({from:sender, to:receiver, value: amount})



```

### useful snippets
https://ethereum.stackexchange.com/questions/2531/common-useful-javascript-snippets-for-geth/3478
