# Getting started with StockPulse SDK

Learn how to integrate real-time stock market data into your application using the StockPulse SDK. This guide helps you set up your environment and make your first data request.

## Prerequisites

Before you begin, ensure that you have the following:
* **Node.js** version 18.0 or later
* A **StockPulse Developer Account**
* A valid **API Key** from your [StockPulse Dashboard](https://example.com/dashboard)

## Install the SDK

Use the following command to add the SDK to your project:

```bash
npm install stockpulse-sdk
```

## Initialize the client

To interact with the StockPulse API, you must initialize the client with your API key.

```JavaScript
const StockPulse = require('stockpulse-sdk');

// Initialize the client
const client = new StockPulse({
  apiKey: '<YOUR_API_KEY>'
});
```
## Fetch a stock quote
Use the getQuote method to retrieve the current price of a specific stock. The following example fetches the price for TCS.

```JavaScript
// Fetch real-time data for Tata Consultancy Services
client.getQuote('TCS')
  .then(quote => {
    console.log(`Current Price: ${quote.price}`);
  })
  .catch(error => {
    console.error('Error fetching quote:', error);
  });
```

## 🚀 Step 3: Publish to GitHub Pages

Once you are happy with your draft, you can publish it to the web. Docusaurus has a built-in command for this.

1.  **Create** a repository on GitHub named `my-sdk-docs`.
2.  **Push** your local code to that repository.
3.  **Update** the `docusaurus.config.js` file with your GitHub organization and project name.
4.  **Run** the deployment command:
    ```bash
    npm run deploy
    ```

