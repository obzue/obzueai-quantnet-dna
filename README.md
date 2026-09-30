# ObzueAI QuantNET DNA

Live market desk. The name is unchanged. Ranked crypto, index and stock quotes, NFT floors, a signed exchange, a paper trading bot, and an art studio for launch plates.

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

Chain clients such as go-ethereum are references only. They are not vendored. NFT generators are not vendored either. See `docs/nft-art.md`.

## Markets

- Crypto ranked by size, largest first, with the full list paged
- Live candles, order book, and prints from the public OKX USDT book
- Featured pairs: BTC, ETH, SOL, XRP, DOGE, ADA, AVAX, LINK, DOT, ATOM, NEAR, APT, SUI, TON, LTC, BCH, UNI, AAVE, ARB, OP, INJ, TIA, PEPE, WIF, BONK, FET
- Indices and listed stocks, including the S&P 500, Nasdaq, and Dow
- NFT collection floors from public Solana marketplace stats
- Email confirmation on signup. That code is for the login only. It never contains wallet words.

## Trading bot

The bot page reads the same public price as the exchange. While the page is open and the wallet is unlocked, a rule can buy or sell inside the QuantNET account:

- Momentum against the last 20 closes
- Mean revert when price is stretched from that average
- A 0.4% grid that resets its anchor on each fill

Fills are signed locally. They are not orders on OKX, a broker, or a chain. A separate button can ask for a one-shot written brief. The brief does not trade.

## Art studio

Launch profiles and seals are drawn in the browser from a theme, a style, and a seed. The same seed redraws the same plate. An optional render stores an image link on the account when image credits are available. Sketches do not need that.

Themes: quantum lattice, abyssal tide, desert sigil, night market, botanical seal, glacial archive, solar myth, ink portrait, circuit relic, lunar mosaic, chrome relic, stained myth.

Styles: layered portrait, field composition, trait card, ink wash, pixel relic, stained glass, editorial poster, orbital oil, brutal plate, heraldic crest.

## Account

Email, Google, and X sign-in. Personal, business, and corporate profiles. Community posts, replies, likes, and follows. Do not post a seed phrase.
