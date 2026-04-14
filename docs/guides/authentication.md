# Authenticating the client

Before you can fetch market data, you must authenticate your requests using a valid API key. This guide shows you how to retrieve your key and configure the SDK.

## Retrieve your API key

1. **Sign in** to the [StockPulse Developer Portal](https://example.com/login).
2. **Navigate** to the **Security** tab in your dashboard.
3. **Select** **Generate New Key**.
4. **Copy** the key and store it in a secure location, such as an environment variable.

## Configure the client

The StockPulse SDK uses a constructor to set your credentials. 

### Best practice: Use environment variables
To keep your credentials secure, do not hard-code your API key. Instead, use an environment variable.

```javascript
const StockPulse = require('stockpulse-sdk');

// Load your key from a secure environment variable
const client = new StockPulse({
  apiKey: process.env.STOCKPULSE_API_KEY
});
```

## Verify authentication

To verify that your key is active, call the testConnection method.

```javascript
try {
  const status = await client.testConnection();
  console.log('Authentication successful:', status);
} catch (error) {
  console.error('Authentication failed. Check your API key and permissions.');
}
```