# `protostar-toolchain` Action

This GitHub Action installs [Protostar](https://github.com/software-mansion/protostar), a StarkNet smart contract development toolchain.

## Example Workflow

```
on: [push]

name: test

jobs:
  check:
    name: Protostar project
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
        with:
          submodules: recursive

      - name: Install Protostar
        uses: sambarnes/protostar-toolchain@main

      - name: Run tests
        run: protostar test
```