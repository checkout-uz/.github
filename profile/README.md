<div align="center">

<img src="https://checkout.uz/assets/img/app-icon.png" width="88" alt="CHECKOUT.UZ" />

# CHECKOUT.UZ

**Payment infrastructure for Uzbekistan.** One integration for Payme, Click, Uzum, Paynet, Xazna, Plum, OSON, Uzcard/Humo cards and more.

[![Website](https://img.shields.io/badge/website-checkout.uz-0969da?style=for-the-badge)](https://checkout.uz)
[![API Docs](https://img.shields.io/badge/docs-API%20v1%20%2F%20v2-6f42c1?style=for-the-badge)](https://checkout.uz/api-docs)

<br/>

[![Active Merchants](https://img.shields.io/endpoint?url=https%3A%2F%2Fcheckout.uz%2Fbadges%2Fmerchants.json&style=for-the-badge)](https://checkout.uz)
[![Active Users](https://img.shields.io/endpoint?url=https%3A%2F%2Fcheckout.uz%2Fbadges%2Fusers.json&style=for-the-badge)](https://checkout.uz)
[![Transactions](https://img.shields.io/endpoint?url=https%3A%2F%2Fcheckout.uz%2Fbadges%2Ftransactions.json&style=for-the-badge)](https://checkout.uz)

<sub>Live numbers, updated automatically straight from production.</sub>

</div>

<br/>

## What we do

CHECKOUT.UZ is a merchant payment gateway for Uzbekistan — one API and one dashboard in front of every major local payment provider, so a business integrates once instead of nine times.

## Official SDKs

One client per language, each exposing both **API v1** and **API v2** through a single object (`client.v1` / `client.v2`), plus a separate client for account-level endpoints that use a different credential.

| Language | Repository | Package |
|---|---|---|
| Python | [checkout-sdk-py](https://github.com/checkout-uz/checkout-sdk-py) | `pip install git+https://github.com/checkout-uz/checkout-sdk-py.git` |
| PHP | [checkout-sdk-php](https://github.com/checkout-uz/checkout-sdk-php) | via Composer |
| JavaScript / Node.js | [checkout-sdk-js](https://github.com/checkout-uz/checkout-sdk-js) | zero dependencies, native `fetch` |
| TypeScript | [checkout-sdk-ts](https://github.com/checkout-uz/checkout-sdk-ts) | zero dependencies, native `fetch` |
| Java | [checkout-sdk-java](https://github.com/checkout-uz/checkout-sdk-java) | Maven / `org.json` |
| C# / .NET | [checkout-sdk-csharp](https://github.com/checkout-uz/checkout-sdk-csharp) | zero dependencies, `System.Text.Json` |
| Go | [checkout-sdk-go](https://github.com/checkout-uz/checkout-sdk-go) | `go get github.com/checkout-uz/checkout-sdk-go` |
| Ruby | [checkout-sdk-ruby](https://github.com/checkout-uz/checkout-sdk-ruby) | RubyGems |

```python
from checkout_uz import CheckoutClient

client = CheckoutClient(api_key="shop_api_key")
payment = client.v2.create_payment(amount=50000, description="Order #1")
print(payment["payment"]["_url"])  # send the customer here
```

Every SDK ships with a fully-mocked test suite (no live API calls) and an MIT license.

## API

- **v1** — `https://checkout.uz/api/v1` — create/check payments, balance, history, stats, direct card pay.
- **v2** — `https://checkout.uz/api/v2` — everything in v1, plus idempotency keys, pagination, cancel/refund, fiscal receipts, and account-level endpoints across all of a merchant's shops.

Full reference: [checkout.uz/api-docs](https://checkout.uz/api-docs)

## License

All SDKs in this organization are released under the [MIT License](https://github.com/checkout-uz/checkout-sdk-py/blob/main/LICENSE).

<div align="center">
<sub>Built by the CHECKOUT.UZ team — <a href="https://checkout.uz">checkout.uz</a></sub>
</div>
