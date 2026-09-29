# Skill set — ObzueAI QuantNET DNA

Reviewed public repositories, what each skill is for, and how this desk uses the idea without copying the code.

## Wallet

- Record three sandbox assets and a per-account ledger.
- Send only to another handle in the same database.
- Show a simulated address that is a label, not a chain destination.

## Exchange

- Immediate swap of QDNA or QNET against QUSD at a published mark.
- Fee depends on account kind: personal 0.30%, business 0.18%, corporate 0.08%.
- Tape stores pair, side, amount, mark, and handle. It does not store email.

## Social

- Posts, comments, an appreciate counter, and follows.
- Authors can remove their own posts.

## Marketplace and NFTs

- Treasury samples for tokens, a meme, and one-per-desk seals.
- Launchpad records a name, symbol, description, layer tag, supply, and QUSD price.
- NFT supply is forced to 1. Reserved symbols: QDNA, QUSD, QNET.
- A purchase moves QUSD from buyer to issuer and quantity between holdings.

## Mining simulation

- One credit about every four seconds, sized by account kind.
- Ledger note is `Simulation tick`. There is no hash rate.

## Documentation

- In-product docs cover accounts, the ledger, swaps, social, launch, the three layers, the session security model, stored data, and launch limits.
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

## What a real worldwide system would still need

A licensed entity where the law requires one, a custody design, independent review, and a decision about whether any asset should exist outside this database. Until then every number is a demonstration figure.
