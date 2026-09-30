# Trading bot skill set

The bot is a rule engine on public prices. It fills the signed-in QuantNET account. It does not place orders on an exchange.

## Data

- Crypto last price, 1-minute candles, book, and prints: public OKX spot `SYMBOL-USDT` market data. Read only. No API key. No order endpoint.
- Ranked coins and global stats: Coinlore.
- Indices and stocks: public Yahoo chart endpoint, only on the exchange equity book. The bot itself trades crypto pairs.
- Charts: TradingView lightweight-charts, already used by the exchange.

## Rules

| Rule | Buy | Sell |
| --- | --- | --- |
| Momentum | Last price above the 20-close average by about 0.15% | Price back under the average, and the account holds the pair |
| Mean revert | Price more than about 0.3% under the average | Price more than about 0.3% above the average |
| Grid | Price 0.4% under the anchor | Price 0.4% above the anchor |

The anchor starts at the price when the bot is armed. A fill sets a new anchor.

## Limits

- Runs only while the bot page is open.
- Checks about every 20 seconds.
- Will not fill again for 45 seconds.
- Each fill is signed by the key in the browser, the same message as a manual exchange order.
- Email must be verified and the wallet must be unlocked.
- Size is a QUSD notional. A sell cannot exceed the live holding.
- Sandbox balances can fall. This is not investment advice and not a brokerage.

## Strategist note

Ask for a brief sends the symbol, last price, session change, 20-bar average, and the rule name. One request. It returns two short paragraphs. It does not arm the bot and it does not sign an order.
