## What is Puzzl3s?

Puzzl3s 🧩 is an engaging collection of web3-based puzzles and Capture The Flag (CTF) challenges. While I didn't create the CTFs themselves, this repository showcases my solutions and serves as a comprehensive resource for other developers and security enthusiasts.

## CTFs

The following challenges are being or have been solved:

- [Damn Vulnerable DeFi V4](docs/DamnVulnerableDeFiV4.md)
- [EthernautCTF](docs/ethernaut-ctf/EthernautCTF.md)
- [QuillCTF](docs/QuillCTF.md)

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
pnpm run build
```

Run all the exploits using:

```sh
pnpm run exploits
```

Note that you can also run the exploit of a specific contract using while also showing traces. Here's an example:

```sh
forge test -vvvv --match-contract RoadClosed
```
