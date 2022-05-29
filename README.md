# `protostar-toolchain` Action

This GitHub Action installs [Protostar](https://github.com/software-mansion/protostar).

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
        uses: sambarnes/protostar-toolchain@v1

      - name: Run tests
        run: protostar test
```