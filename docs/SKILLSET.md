# Skill set — ObzueAI QuantNET DNA

Reviewed public repositories, what each skill is for, and how this desk uses the idea without copying the code.

Later notes live beside this file:

- [docs/nft-art.md](nft-art.md) — generative plate engine and the NFT repositories that were read, not installed.
- [docs/trading-bot.md](trading-bot.md) — paper bot, live books, and the three rules.

## Wallet

- Record three sandbox assets and a per-account ledger.
- Send only to another handle in the same database.
- Show a simulated address that is a label, not a chain destination.
- A 24-word key is generated in the browser. Only the public address is stored after a signed registration.

## Exchange

- Signed buys and sells of live crypto and listed names, filled inside the QuantNET account at the public price.
- Fee depends on account kind: personal 0.30%, business 0.18%, corporate 0.08%.
- Tape stores pair, side, amount, mark, and handle. It does not store email.
- Featured USDT books are listed in the README. Candles refresh on the exchange.

## Trading bot

- Momentum, mean revert, and grid. See trading-bot.md.
- Runs only while its page is open. Each fill is signed by the local key.
- A strategist brief is one request and does not trade.

## Social

- Posts, comments, an appreciate counter, and follows.
- Authors can remove their own posts.

## Marketplace, NFTs, and the studio

- Treasury samples for tokens, a meme, and one-per-desk seals, each with a generated plate.
- Live Solana collection floors are a separate read-only board.
- Launchpad records a name, symbol, description, layer tag, supply, QUSD price, theme, style, and seed.
- NFT supply is forced to 1. Reserved symbols: QDNA, QUSD, QNET.
- Optional rendered images are stored as links, capped per hour. Sketches do not call an image model.
- Generators that were read and not installed: HashLips art engine, HashLips generative-art-node, NotLuksus nft-art-generator, HashLips Lab art-engine.

## Mining simulation

- One credit about every four seconds, sized by account kind.
- Ledger note is `Simulation tick`. There is no hash rate.

## Documentation

- In-product docs cover accounts, the ledger, swaps, the bot, the studio, social, launch, the three layers, the session security model, stored data, and launch limits.
- Search filters those sections and the repository notes.

## Security and KYC

- Server functions require the session. The browser does not choose the user id.
- Value moves in one SQL statement so debit and credit stay together.
- Attestation is `unreviewed`, `self`, or `business`. It is not a government identity check, sanctions screen, or license to hold customer funds.
- Contract static analysis (Slither) and OpenZeppelin access-control patterns were reviewed so they would not be confused with this website's session model. Neither is embedded.

## Layer references (not cloned)

| Layer | Repository | Why it was reviewed |
| --- | --- | --- |
| L1 | [ethereum/go-ethereum](https://github.com/ethereum/go-ethereum) | What a real settlement client contains |
| L2 | [ethereum-optimism/optimism](https://github.com/ethereum-optimism/optimism) | Rollup derivation versus an app database |
| L2 | [OffchainLabs/nitro](https://github.com/OffchainLabs/nitro) | Fraud-proof style scaling |
| L3 | [lightningnetwork/lnd](https://github.com/lightningnetwork/lnd) | Channels above a base chain |
| Stablecoin | [circlefin/stablecoin-evm](https://github.com/circlefin/stablecoin-evm) | Fiat-token controls that this desk does not implement |
| Contracts | [OpenZeppelin/openzeppelin-contracts](https://github.com/OpenZeppelin/openzeppelin-contracts) | Token interfaces, not copied |
| Security | [crytic/slither](https://github.com/crytic/slither) | Solidity and Vyper static analysis |
| DeFi surface | [WaykiChain/WaykiChain](https://github.com/WaykiChain/WaykiChain) | A chain that advertises DEX and stablecoin modules |
| Quantum | [Qiskit/qiskit](https://github.com/Qiskit/qiskit) | Circuit SDK. Not a payments rail. Not wired in. |
| Quantum | [quantumlib/Cirq](https://github.com/quantumlib/Cirq) | NISQ circuits. Not asset custody. |
| Quantum | [PennyLaneAI/pennylane](https://github.com/PennyLaneAI/pennylane) | Differentiable quantum programming. Not connected to balances. |
| NFT art | [HashLips/hashlips_art_engine](https://github.com/HashLips/hashlips_art_engine) | Layered generation. Not installed. |
| NFT art | [NotLuksus/nft-art-generator](https://github.com/NotLuksus/nft-art-generator) | Weighted traits and metadata. Not installed. |
| Charts | [tradingview/lightweight-charts](https://github.com/tradingview/lightweight-charts) | Candle drawing only. |

## What a real worldwide system would still need

A licensed entity where the law requires one, a custody design, independent review, and a decision about whether any asset should exist outside this database. Until then every number on the desk is a demonstration fill at a public price, not a brokerage order.
