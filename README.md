# market dash

A simple dashboard for financial markets

Essentially follows [this medium article](https://medium.com/geekculture/how-to-create-a-simple-crypto-dashboard-using-python-b9678e7867b) with some differences. TODO: explain the differences.


## Possible data sources

WARNING: likely all of these sources are 15 min delayed or more on free tiers. TODO: check this.

### Alpaca

Link: [Alpaca python package](https://github.com/alpacahq/alpaca-py)

- crypto + stocks
- Free 200 API calls/min
- official

Cons:

- Some mixed reports of user experience, no dealbreakers

Decision: start with Alpaca due to sufficient free API calls for development.

### Polygon

Link: [Polygon python package](https://github.com/polygon-io/client-python)

Features:

- crypto + stocks
- official

Cons:

- Only 5 free API calls/min

Decision: too few free API calls/min to experiment in the early stages. Use Polygon later if problems with Alpaca arise.

### Binance API

Link: [Binance python api](https://github.com/binance/binance-connector-python)
(see [the docs here](https://github.com/binance/binance-spot-api-docs) for other languages)

Features:

- crypto
- official wrapper around official binance api

Cons:

- no stocks

Decision: could be used as a robust second source for crypto data.

### Interactive brokers

Link: [ib_insync](https://github.com/erdewit/ib_insync)

Features:

- stocks
- wrapper for interacting with IB official API

Cons:

- no crypto on IB
- unofficial

Decision: could be used as a robust second source for stock data.

### Yahoo finance

Link: [yfinance](https://github.com/ranaroussi/yfinance)

Features:

- crypto + stocks scraping

Cons:

- scraping + yahoo finance itself not being a direct source
- unofficial, has lead to occasional breakages when yahoo changes their encryption

Decision: Consider including as a backup source of data when timing isn't critical. Low priority.