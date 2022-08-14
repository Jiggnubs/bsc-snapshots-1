# *bsc-snapshots*


*\> [geth-snapshots](#geth-snapshots)*

*\> [erigon-snapshots](#erigon-snapshots)*

Updated every ~24~ 36 hours

Old snapshot deleted ~1~ 12 hours after new snapshot generated

## geth-snapshots


> Database uses [geth(v1.1.12)](https://github.com/bnb-chain/bsc/releases/tag/v1.1.12) for sync


### download

<!-- begin_geth -->

!!! from block [20426388](https://bscscan.com/block/20426388)
```bash
aria2c -s14 -x14 -k100M https://snapshots.bnb48.club/geth.20426388.tar.lz4 -o geth.tar.lz4
```


### checksum


!!! db size 563.33 gb, 575.55 gb after decompression
```bash
> openssl sha256 geth.tar.lz4
SHA256(geth.tar.lz4)= 6826ad3e86e7350e6e13bb2e38d0221cd6379352ad24887c18c8d0c8325eea6b
```

<!-- end_geth -->

### uncompress


running a script: _`lz4 -cd geth.tar.lz4 | tar xf -`_


### flags


```bash
--txlookuplimit=0 --diffsync=true --syncmode=full --tries-verify-mode=none --pruneancient=true --diffblock=5000
```


## erigon-snapshots


> Database uses [erigon(v2022.07.04)](https://github.com/ledgerwatch/erigon/releases/tag/v2022.07.04) for sync


### download

<!-- begin_erigon -->

!!! from block [20422653](https://bscscan.com/block/20422653)
```bash
aria2c -s14 -x14 -k100M https://snapshots.bnb48.club/erigon.20422653.tar.lz4 -o erigon.tar.lz4
```


### checksum


!!! db size 754.86 gb, 1081.61 gb after decompression
```bash
> openssl sha256 erigon.tar.lz4
SHA256(erigon.tar.lz4)= 92b7e8f09f873438254531e678a0e47b811b3263ec6d55a7cc2c4d3e69ca7993
```

<!-- end_erigon -->

### uncompress


running a script: _`lz4 -cd erigon.tar.lz4 | tar xf -`_


### flags


```bash
--chain=bsc --prune= --prune.h.older=5000 --prune.r.older=5000 --prune.t.older=5000 --prune.c.older=5000 --db.pagesize=16k
```
