# oanda-open-api-spec

> **Experimental.** This is a work-in-progress effort and is not guaranteed to be accurate or complete.

An unofficial OpenAPI 3.1 specification for the [OANDA v20 REST API](https://www.oanda.com/lca-forex/api).

## What this is

OANDA ships their developer docs as an OpenAPI 2 (Swagger) spec that is incomplete and, in places, out of sync with the live API. This repo is an attempt to:

- Convert that spec to **OpenAPI 3.1**
- Fill in **missing endpoints** and correct schemas by cross-referencing the [live API documentation](https://developer.oanda.com/docs/oanda-api/)
- Produce something closer to a spec you can actually use for code generation or client tooling

## Coverage

The spec currently documents **30 endpoints** across 7 domains:

| Domain | Description |
|---|---|
| Account | Account details, summary, instruments, configuration, and changes |
| Orders | Create, list, cancel, and manage orders |
| Trades | Open, close, list, and manage individual trades |
| Positions | View and close positions per instrument |
| Transactions | Query transaction history and stream live transactions |
| Pricing | Current prices and streaming price feeds |
| Instruments | Historical and latest candlestick data |

## Servers

| Environment | Base URL |
|---|---|
| Live Trading | `https://api-fxtrade.oanda.com/v3` |
| Practice Trading | `https://api-fxpractice.oanda.com/v3` |
| Live Streaming | `https://stream-fxtrade.oanda.com/v3` |
| Practice Streaming | `https://stream-fxpractice.oanda.com/v3` |

## Auth

All requests require a Bearer token obtained from the OANDA Account Management Portal. The spec defines this as the `authorization` security scheme.

## Status / Known Gaps

This is actively being built out. Known areas that still need work:

- Streaming endpoint request/response bodies are not fully modeled
- Not all error response codes are documented for every endpoint
- Some schema fields may be missing or typed loosely compared to the live API

Contributions and corrections are welcome.

## License

MIT
