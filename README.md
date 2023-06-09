![Lint workflow status](https://img.shields.io/github/actions/workflow/status/leovct/puzzl3s/lint.yml?branch=main&label=ci-lint)
![Exploit workflow status](https://img.shields.io/github/actions/workflow/status/leovct/puzzl3s/exploit.yml?branch=main&label=ci-exploit)

## What is Puzzl3s?

Puzzl3s 🧩 is an engaging collection of web3-based puzzles and Capture The Flag (CTF) challenges. While I didn't create the CTFs themselves, this repository showcases my solutions and serves as a comprehensive resource for other developers and security enthusiasts.

## Challenges

The following challenges have been solved:

- [QuillCTF](doc/QuillCTF.md)

## Exploit

First, make sure the following are installed:

1. [Foundry](https://book.getfoundry.sh/getting-started/installation) which comes with [Forge](https://book.getfoundry.sh/forge/), an Ethereum testing framework, to build smart contracts and run the exploits.
2. [Huff compiler](https://docs.huff.sh/get-started/installing/) which is needed for huff puzzles such as [CollatzPuzzle](src/QuillCTF/CollatzPuzzle.sol).

In order to build and run the exploits, first clone the Github repository:

```sh
git clone https://github.com/leovct/puzzl3s
cd puzzl3s
```

To build the contracts, you can run the following command:

```sh
make build
```

Run all the exploits using:

```sh
make exploit
```

Note that you can also run the exploit of a specific contract using `CONTRACT=<CONTRACT_NAME>` (see `make list`) and you can show traces using `DEBUG=TRUE`. Here's an example:

```sh
make exploit CONTRACT=RoadClosed DEBUG=TRUE
```

To discover all the possible commands, run:

```sh
make
```
