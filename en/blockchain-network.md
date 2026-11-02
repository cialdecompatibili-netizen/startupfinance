---
layout: single
title: "Blockchain network: a network built on existing software"
permalink: /en/startup/blockchain-network/
ref: rete-blockchain
author_profile: false
description: "Idea under study: a blockchain network for payments and crypto startups, built from software with permissive licenses."
lang: en
locale: en
tr: tradotto
tr_hash: 1hw8xtv
---

<p class="hub-lead"><span class="hub-tag">Idea under study</span> A blockchain network of our own, designed for fast, low-cost payments and to host the startups on this site. We do not start from zero and we do not copy at random: we start from ready-made software with simple licenses.</p>

## How the network works
The network uses a few known validators that produce blocks in turn (**delegated proof of stake**) and a virtual machine compatible with Ethereum's. Resources are not only paid as fees: they can be quota-based, obtained by locking tokens.

The three basic ideas:
1. **Few known validators taking turns**: fast and predictable, less decentralized than Bitcoin or Ethereum.
2. **Compatibility with Ethereum tools**: existing wallets, libraries and contracts work.
3. **Quota-based resources**: whoever uses the network a little pays little or nothing, whoever uses it a lot locks value. Useful for payments.

## The license knot
Using other people's code means respecting its license. With **LGPL** and **GPL**, changes to the covered code must be released under the same terms, with obligations on notices and license. For a project that later wants to sell services and keep something proprietary, this is a constraint to understand well, so we start from components with permissive licenses and get legal review.

## Three paths, from simplest to most complex
| Path | What you take | License | Check |
|---|---|---|---|
| **A. EVM network on Reth** | Ethereum node written in Rust, modular, usable as a library | Apache-2.0 and MIT (permissive) | Confirmed on the repository |
| **B. Network with Cosmos SDK and CometBFT** | Blockchain with rotating validators | Apache-2.0 (as far as we know) | To verify on the repository |
| **C. Fork of go-ethereum** | The most widely used Ethereum node | LGPL library, GPL programs (as far as we know) | To verify: licenses with obligations |

As a rule: **Apache-2.0 and MIT** are the most convenient (you can even keep your own code closed, while keeping notices and license). **LGPL and GPL** require publishing changes. Some projects also use "business source" licenses that limit commercial use: before adopting any code, we read the LICENSE file of the exact version we use.

## What we propose
**Path A as the first choice.** An Ethereum-compatible network built on Reth, with a few rotating validators, and quota-based resources only if needed. Reasons: permissive licenses, ready-made tools, no need to write a node from scratch. Path B remains the alternative if we need a network with very custom rules.

## How we proceed, in phases
1. **Local test network**: we start a node and a few validators on our own computer, no real value.
2. **Public test network** with 3-5 validators chosen by us, for the first payment tests.
3. **Registry and payments for our own projects**: we use the network for [Immutable registry]({{ '/en/startup/immutable-registry/' | relative_url }}) and [Physical network]({{ '/en/startup/physical-network/' | relative_url }}).
4. **Opening to other validators and developers**, only after a security audit and legal opinion.

## What the network can offer
- Low-cost stablecoin payments and transfers.
- Space for the crypto startups on this site: contracts, registries and dated proofs.
- Developer tools: documentation, wallets and a test faucet.
- Services for whoever wants to launch their own app without running a node.

## How we could earn
Fees on the services we build on top of the network, subscriptions for those who use the registry and payments, consulting for those who want to start their own network. Prices not defined. No token to sell in order to start.

## Risks and rules to verify
- **Security**: a blockchain handles real value. External audits and a long test period are needed before opening it.
- **Licenses**: an opinion from a lawyer experienced in free software on the final combination of components.
- **Tokens and sales**: issuing or selling a token may fall under rules such as MiCA and Italian ones. For now nothing is issued.
- **Anti-money laundering**: fast, low-cost networks also attract illicit use; clear rules and cooperation with authorities are needed. See the [Crypto Magazine articles](https://cialdecompatibili-netizen.github.io/cryptomagazine/en/blog/) on how illicit flows move from one service to another.
- **Competition**: many similar networks already exist. Our possible difference is a precise use (registries and payments for small Italian businesses), not being "just another generic network".

## Status
Idea under study: no active network, no token for sale and no promise of returns. If you want to join with time or capital, read the [Invest]({{ '/en/invest/' | relative_url }}) page.

<p><a class="hub-btn hub-btn--a" href="{{ '/en/invest/?startup=rete-blockchain' | relative_url }}">Invest</a> <a class="hub-btn hub-btn--o" href="{{ '/en/work-with-us/?startup=rete-blockchain' | relative_url }}">Apply</a></p>
