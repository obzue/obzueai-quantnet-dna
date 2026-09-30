# ObzueAI QuantNET DNA

Live market desk. The name is unchanged. Ranked crypto, index and stock quotes, NFT floors, and a signed exchange. The wallet is self-custody.

## Keys

Users own their keys. Setup is a 24-word BIP39 phrase generated in the browser.

- QuantNET does not hold keys.
- QuantNET does not keep a backup copy.
- The phrase is not emailed, posted, or written to the database.
- The server stores only the public address after the user signs a registration message.
- If the words are lost, nobody at QuantNET can restore them.

Libraries installed from the audited upstream packages, not cloned into this repo:

- [paulmillr/scure-bip39](https://github.com/paulmillr/scure-bip39)
- [paulmillr/scure-bip32](https://github.com/paulmillr/scure-bip32)
- [paulmillr/noble-curves](https://github.com/paulmillr/noble-curves)
- [bitcoin/bips BIP39](https://github.com/bitcoin/bips/blob/master/bip-0039.mediawiki)
- [tradingview/lightweight-charts](https://github.com/tradingview/lightweight-charts)

Chain clients such as go-ethereum are references only. They are not vendored.

## Markets

- Crypto ranked by size, largest first, with the full list paged
- Live candles, order book, and prints where the venue publishes them
- Indices and listed stocks, including the S&P 500, Nasdaq, and Dow
- NFT collection floors
- Email confirmation on signup. That code is for the login only. It never contains wallet words.

## Trading

The wallet opens on its own screen. Orders on the exchange are signed by that key and filled in the QuantNET account at the live price. A fill is not a broadcast onto Bitcoin or Ethereum.

## Account

Email, Google, and X sign-in. Personal, business, and corporate profiles. Community posts, replies, likes, and follows. Do not post a seed phrase.
