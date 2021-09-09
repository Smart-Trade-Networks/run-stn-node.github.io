# Chapter 1 - Setting up an STN Node
# Introduction

Smart Trade Networks currently runs a Proof of Authority EVM blockchain.

You can view the networks stats here: [http://54.206.103.22:8000/#stats](http://54.206.103.22:8000/#stats)

Simple Blockchain Explorer here: [http://65.21.7.175:8000/](http://65.21.7.175:8000/)

If you hold more than 500 STNs we will send you a plug and play computer that run an STN node.

## Steps to Run a Node
These are the high level steps to run your own node.

1. Install Geth
2. Download and init the the STN genesis file.
3. Start Geth

## 1. Instal Geth

The instructions to install Geth are located [here](https://geth.ethereum.org/docs/install-and-build/installing-geth).

## 2. Download and init genesis file

Download the [stn.json](./stn.json) genesis file.

Then init the file by running the following command.

```bash
geth --datadir=$HOME/.beefledger init beefledger.json
```

## 3. Start Geth

You can start geth with the following command or you could download it as a bash script.


```bash
#!/bin/bash
geth --networkid=18122 \
--datadir=$HOME/.beefledger \
--cache=1024 \
--syncmode=full \
--ethstats='Brisbane_Node:delva57@54.206.103.22:8080' \
--bootnodes="enode://6ce750dd33c4bed7ee148ed5d70f52806c164da1263d2d7e9d9f9c296671ae3178eb93fb433628e49406b6ef6ff658cb2bf55628d6c785d80ce3bd9f549ca2d3@13.236.201.188:30303","enode://73a2c9708649e6d211a0708161dc3737badbc08d919106b12a30f9e22813881b707e345d76f25f48efe1d884be3fbdda3d181c024eae565e9e4a83924bba7c94@3.104.36.254:30303","enode://c2c9492c7dee6dce7b9d6c335b03fa571ca422a55adb4085abb8108bb750313748294a88803698f3c16a5a26235b44ff1c835273d6b9bccf263a08cc12093672@54.206.122.5:30303","enode://42e12e301ee17a75027c8d7dfdec072a8d7ec87fbd4b80042f7a568803896579052b188806c2d83e00cd9c75060b8a62b6bea479ab8958d377b6fa8a94a96a33@54.206.103.22:30305","enode://aade8d01823ec53e3f4ddeb1f001aa971f72e2a4b015d222aafbd8efcfc4a0d7bb022824eb47bd694c6a83a5856021a231ceb529572c8b4e82e52e6f690fd93b@127.0.0.1:30301" \
--rpc \
--rpcapi="admin,eth,net,web3,personal" \
```


The mdBook source and documentation are released under
the [Mozilla Public License v2.0](https://www.mozilla.org/MPL/2.0/).

