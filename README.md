<!---
[![Build Status](https://github.com/atomone-hub/atonevanity/workflows/Tests/badge.svg?branch=master)](https://github.com/atomone-hub/atonevanity/actions?query=workflow%3ATests+branch%3Amaster+event%3Apush)
[![codecov.io](https://codecov.io/gh/atomone-hub/atonevanity/branch/master/graph/badge.svg)](https://codecov.io/gh/atomone-hub/atonevanity)
-->

# cosmosvanity

> CLI tool for generating [Atone](https://atom.one) vanity addresses
> Fork of CosmosVanity.

## Features
* Generate AtomOne (atone1...) bech32 vanity addresses
* Use all CPU cores
* Specify a substring that the addresses must
    * start with
    * end with
    * contain
* Set required minimum amount of letters (a-z) or digits (0-9) in the addresses
* Binaries built for Linux, macOS and Windows

## Installing
Download the latest binary release from the [_Releases_](https://github.com/atomone-hub/atonevanity/releases) page. Alternatively, build from source yourself.

## Usage examples
Find an address that starts with "00000" (e.g. atone100000v3fpv4qg2a9ea6sj70gykxpt63wgjen2p)
```bash
./cosmosvanity --startswith 00000
```

Find an address that ends with "8888" (e.g. atone134dck5uddzjure8pyprmmqat96k3jlypn28888)
```bash
./cosmosvanity --endswith 8888
```

Find an address containing the substring "gener" (e.g. atone1z39wgener7azgh22s5a3pyswtnjkx2w0hvn3rv)
```bash
./cosmosvanity --contains gener
```

Find an address consisting of letters only (e.g. atone1rfqkejeaxlxwtjxucnrathlzgnvgcgldzmuxxe)
```bash
./cosmosvanity --letters 38
```

Find an address with at least 26 digits (e.g. atone1r573c4086585u084926726x535y3k2ktxpr88l)
```bash
./cosmosvanity --digits 26
```

Generate 5 addresses (the default is 1)
```bash
./cosmosvanity -n 5
```

Restrict to using only 1 CPU thread. This value defaults to the number of CPUs available.
```bash
./cosmosvanity --cpus 1
```

Combine flags introduced above
```bash
./cosmosvanity --contains 8888 --startswith a --endswith c
```
