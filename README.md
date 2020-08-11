# PyTrader
Predictious trading bot that streams market data of specific instruments to buy or sell them (back-end for Falcon). Gets data using **TradingView webhook API** which sends a **JSON** message to an **AWS Lambda** function, this executes a **Python** script running through the **AWS Chalice Serverless Framework**. The **Python** script then executes a bracket order using the **Alpaca API Paper Trading API**. Tested requests using **Insomnia REST API Client**.

### Demo:
#### 1. Deploy Chalice REST API using CMD
<img src="https://user-images.githubusercontent.com/66835262/89742956-abb04300-da6c-11ea-949a-99d3a8325219.png" width="800px">

<br />

#### 2. Set up alerts using Trading View and set Webhook URL to Chalice REST API URL
<img src="https://user-images.githubusercontent.com/66835262/89742871-bc13ee00-da6b-11ea-9d8c-ee2e4bcfa645.png" width="800px">

<br />

#### 3. Wait till alarm is triggered and orders are placed through Alpaca
<img src="https://user-images.githubusercontent.com/66835262/89742880-d948bc80-da6b-11ea-90c3-58d0c3d9cfc7.png" width="800px">

### Resources Used: 
* **TradingView webhooks:** https://www.tradingview.com/support/solutions/43000529348-i-want-to-know-more-about-webhooks/
* **AWS Chalice Framework for Serverless Python:** https://github.com/aws/chalice
* **Alpaca API:** https://alpaca.markets/docs/api-documentation/api-v2/
