# AI Market Cap

**A free pre-earnings stock scanner for AI and tech stocks.**
Live site: **https://aismarketcap.com**

AI Market Cap watches the earnings calendar for AI, semiconductor and tech names and scores each one *before* the print. Every morning it publishes the day's list: which names are reporting, how far out their earnings date is, the analyst target, the current price, and a five-factor pre-earnings score.

The daily list is free and needs no account. [Pro](https://aismarketcap.com/pricing) ($5/month or $50/year) unlocks the full target range, the implied move and the stop level for every name in the window, plus the morning email with the top five setups.

👉 **Try it:** https://aismarketcap.com

---

## What it does

- **A real earnings calendar** — every tracked ticker's next report date, counted down to the day, on the homepage and on a per-stock page at `/stock/<TICKER>`.
- **A pre-earnings score (0–100)** — five factors, each one a thing that can actually be measured before a print. See [SCORING.md](SCORING.md).
- **The day's pick and a runner-up** — one name we would trade, one name we'd watch, published every morning with the reasoning and the entry.
- **A morning email** — the top five setups of the day, to subscribers.
- **A wins board** — every call we published, with the entry we published and where it went since. The denominator is on the page too.

## Who it's for

Anyone trading a name in the days before it reports. The scanner is free and public on purpose: the list is the product, and the paid tier is the depth.

## How it's built

- Python for the scanner and the generators; a small Flask app for the live routes; static HTML for every stock, blog and calendar page.
- Market data from Yahoo Finance, analyst consensus and options-implied moves from the same feed, news headlines from Google News.
- Pages are generated, not rendered at request time — so they are fast, cacheable, and readable by a crawler without running anything.

## Data and honesty

- Every number on the site comes from the feed and is stamped when it was read. Nothing is smoothed, and a missing value is shown as missing rather than as zero.
- The wins board shows the call, the entry and the result. It shows how many calls have been published and how many are above their target, so the board can't read as "we never miss".
- Nothing here is investment advice.

## Links

- Site: https://aismarketcap.com
- Pricing: https://aismarketcap.com/pricing
- Contact: aismarketcap.com@gmail.com

## License

MIT — see [LICENSE](LICENSE).
