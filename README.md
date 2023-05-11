# About Lecca
```
LECCA is a crypto-native investment firm that invests in the Web3, digital assets and blockchain companies.
We provide guidance and support to customer-obsessed business.
We spearhead community-centered initiatives for mass adoption of blockchain and cryto
```

Official documentation:
>- [Validator setup instructions](https://docs.nibiru.fi/run-nodes/testnet/)

Explorer:
>- [https://nibiru.explorers.guru](https://nibiru.explorers.guru)

### Minimum Hardware Requirements
 - 4x CPUs; the faster clock speed the better
 - 8GB RAM
 - 100GB of storage (SSD or NVME)

### Recommended Hardware Requirements 
 - 8x CPUs; the faster clock speed the better
 - 64GB RAM
 - 1TB of storage (SSD or NVME)

## Set up your nibiru fullnode
```
wget https://raw.githubusercontent.com/freshe4qa/nibiru/main/nibiru2.sh && chmod +x nibiru2.sh && ./nibiru2.sh
```

<p align="center">
  <img height="100" height="auto" src="https://user-images.githubusercontent.com/50621007/199199328-32dcdc7c-db06-4519-827f-6c6af09228f9.png">
</p>

## Post installation

When installation is finished please load variables into system
```
source $HOME/.bash_profile
```

Synchronization status:
```
nibid status 2>&1 | jq .SyncInfo
```

### Create wallet
To create new wallet you can use command below. Don’t forget to save the mnemonic
```
nibid keys add $WALLET
```

Recover your wallet using seed phrase
```
nibid keys add $WALLET --recover
```

To get current list of wallets
```
nibid keys list
```


Node info
```
nibid status 2>&1 | jq .NodeInfo
```

Show node id
```
nibid tendermint show-node-id
```
