2020-05-15 Upgrade Testnet
==========================

On May 15, 2020 the Bitcoin Cash network will undergo a planned protocol upgrade, as part of a series of regularly scheduled network upgrades. The changes have been implemented three months prior to upgrade activation in order to permit the ecosystem to prepare well in advance.

To assist technical preparations for the upgrade, a testnet is available where the upgrade features can be trialed and tested. Node implementations, wallets, businesses and services built on the Bitcoin Cash network can use this testnet to ensure compatibility, or to get started building products to make use of the upgrade features. This document outlines the information needed to participate in this upgrade testnet.

## Upgrade Testnet Parameters

Fork time: `1586966400`  (April 15, 2020 16:00:00 UTC)

## Set up a node

Prior to starting your node, it is suggested the you delete the ban list at `.bitcoin/testnet3/banlist.dat`

Then run Bitcoin ABC 0.21.4 with:
```
bitcoind -testnet -phononactivationtime=1586966400 -addnode=bitcoincash.gq
```

Alternatively as bitcoin.conf file:
```
testnet=1
addnode=bitcoincash.gq
phononactivationtime=1586966400
```

Then run these commands to ensure you do not sync to regular testnet, which may have more proof-of work,
but instead sync to the upgrade testnet:

```
bitcoin-cli -testnet invalidateblock 0000000000000099fa31071c0794096c5a22aeb62d292495371466c0b9b2c5fe
```

After invalidating the block, the "new" block 1372808 has hash 0000000004dea8a43096a19b1bbad2e42979820fd009bf75f642576234151c89

## Other services

Miners: to `bitcoincash.gq:19338`
user: (testnet address) password:(anything)

Electrumx server: `fulcrum.bitcoincash.gq:60002` will follow the bitcoind.

Explorer: http://bitcoincash.gq:3002

## Communication

To communicate and coordinate with other Upgrade Testnet users, you can join the [Testing Workgroup](workgroup.md) and its associated [Telegram Group](https://t.me/joinchat/DUeWWkYZbVMjvwMTRFlRhw)

