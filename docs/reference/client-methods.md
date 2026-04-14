# Client methods

This page describes the methods available in the `StockPulse` client library.

---

### getQuote

Retrieves the real-time price and daily change for a specific stock symbol.

#### Syntax
```javascript
client.getQuote(symbol)
```
#### Parameters

| Parameter | Type | Required | Description |
|---|---|---|---|
| symbol | String | Yes | The ticker symbol of the stock (for example, TCS or RELIANCE). |

#### Return value

Returns a Promise that resolves to a Quote object.

##### Example

```JavaScript
const quote = await client.getQuote('TCS');
console.log(quote.price);
```

#### Exceptions

| Exception | Description |
|---|---|
| InvalidSymbolException | The provided ticker symbol was not found. |
| RateLimitException | The API request limit for your key has been exceeded.