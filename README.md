# *bsc-snapshots*


*\> [geth-snapshots](#geth-snapshots)*

*\> [erigon-snapshots](#erigon-snapshots)*


## geth-snapshots


> Database uses [geth(v1.1.11)](https://github.com/bnb-chain/bsc/releases/tag/v1.1.11) for sync


### download

<!-- begin_geth -->

!!! from block [18763014](https://bscscan.com/block/18763014)
```bash
aria2c -s14 -x14 -k100M https://snapshots.bnb48.club/geth.18763014.tar.gz -o geth.tar.gz
```


### checksum


!!! db size 523.98 gb, 557.01 gb after decompression
```bash
> openssl sha256 geth.tar.gz
SHA256(geth.tar.gz)= c59fa47806b33cbf8510d247d9fb8f0c27599a99caf41ea42b858fb0aaada8e3
```

<!-- end_geth -->

### uncompress


running a script: _`pigz -dkc geth.tar.gz | tar xvf -`_


### flags


```bash
--txlookuplimit=0 --diffsync --syncmode=snap
```


## erigon-snapshots


> Database uses [erigon(v2022.06.01)](https://github.com/ledgerwatch/erigon/releases/tag/v2022.06.01) for sync


### download

<!-- begin_erigon -->

!!! from block [18758210](https://bscscan.com/block/18758210)
```bash
aria2c -s14 -x14 -k100M https://snapshots.bnb48.club/erigon.18758210.tar.gz -o erigon.tar.gz
```


### checksum


!!! db size 743.95 gb, 1803.00 gb after decompression
```bash
> openssl sha256 erigon.tar.gz
SHA256(erigon.tar.gz)= c593da6689c7a922492c21e8f021064996362dfc95ad424755cf07326d8f9c77
```

<!-- end_erigon -->

### uncompress


running a script: _`pigz -dkc erigon.tar.gz | tar xvf -`_


### flags


```bash
--snapshots=false --prune= --prune.h.older=5000 --prune.r.older=5000 --prune.t.older=5000 --prune.c.older=5000
```
