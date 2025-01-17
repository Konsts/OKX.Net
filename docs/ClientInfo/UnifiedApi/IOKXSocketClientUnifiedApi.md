---
title: IOKXSocketClientUnifiedApi
has_children: true
parent: Socket API documentation
---
*[generated documentation]*  
`OKXSocketClient > UnifiedApi`  
*Unified API*
  

***

## SubscribeToAccountUpdatesAsync  

[https://www.okx.com/docs-v5/en/#trading-account-websocket-account-channel](https://www.okx.com/docs-v5/en/#trading-account-websocket-account-channel)  
<p>

*Subscribe to account information updates. Data will be pushed when triggered by events such as placing/canceling order, and will also be pushed in regular interval according to subscription granularity.*  

```csharp  
var client = new OKXSocketClient();  
var result = await client.UnifiedApi.SubscribeToAccountUpdatesAsync(/* parameters */);  
```  

```csharp  
Task<CallResult<UpdateSubscription>> SubscribeToAccountUpdatesAsync(Action<OKXAccountBalance> onData, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|onData|On Data Handler|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## SubscribeToAdvanceAlgoOrderUpdatesAsync  

[https://www.okx.com/docs-v5/en/#order-book-trading-algo-trading-ws-advance-algo-orders-channel](https://www.okx.com/docs-v5/en/#order-book-trading-algo-trading-ws-advance-algo-orders-channel)  
<p>

*Subscribe to advance algo orders (includes iceberg order and twap order) updates. Data will be pushed when first subscribed. Data will be pushed when triggered by events such as placing/canceling order.*  

```csharp  
var client = new OKXSocketClient();  
var result = await client.UnifiedApi.SubscribeToAdvanceAlgoOrderUpdatesAsync(/* parameters */);  
```  

```csharp  
Task<CallResult<UpdateSubscription>> SubscribeToAdvanceAlgoOrderUpdatesAsync(OKXInstrumentType instrumentType, string symbol, string underlying, Action<OKXAlgoOrder> onData, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|instrumentType|Instrument Type|
|symbol|Symbol|
|underlying|Underlying|
|onData|On Data Handler|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## SubscribeToAlgoOrderUpdatesAsync  

[https://www.okx.com/docs-v5/en/#order-book-trading-algo-trading-ws-algo-orders-channel](https://www.okx.com/docs-v5/en/#order-book-trading-algo-trading-ws-algo-orders-channel)  
<p>

*Subscribe to algo orders (includes trigger order, oco order, conditional order) updates. Data will not be pushed when first subscribed. Data will only be pushed when triggered by events such as placing/canceling order.*  

```csharp  
var client = new OKXSocketClient();  
var result = await client.UnifiedApi.SubscribeToAlgoOrderUpdatesAsync(/* parameters */);  
```  

```csharp  
Task<CallResult<UpdateSubscription>> SubscribeToAlgoOrderUpdatesAsync(OKXInstrumentType instrumentType, string symbol, string underlying, Action<OKXAlgoOrder> onData, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|instrumentType|Instrument Type|
|symbol|Symbol|
|underlying|Underlying|
|onData|On Data Handler|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## SubscribeToBalanceAndPositionUpdatesAsync  

[https://www.okx.com/docs-v5/en/#trading-account-websocket-balance-and-position-channel](https://www.okx.com/docs-v5/en/#trading-account-websocket-balance-and-position-channel)  
<p>

*Subscribe to account balance and position information updates. Data will be pushed when triggered by events such as filled order, funding transfer.*  

```csharp  
var client = new OKXSocketClient();  
var result = await client.UnifiedApi.SubscribeToBalanceAndPositionUpdatesAsync(/* parameters */);  
```  

```csharp  
Task<CallResult<UpdateSubscription>> SubscribeToBalanceAndPositionUpdatesAsync(Action<OKXPositionRisk> onData, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|onData|On Data Handler|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## SubscribeToEstimatedPriceUpdatesAsync  

[https://www.okx.com/docs-v5/en/#public-data-websocket-estimated-delivery-exercise-price-channel](https://www.okx.com/docs-v5/en/#public-data-websocket-estimated-delivery-exercise-price-channel)  
<p>

*Subscribe to the estimated delivery/exercise price of FUTURES contracts and OPTION updates.*  
*Only the estimated delivery/exercise price will be pushed an hour before delivery/exercise, and will be pushed if there is any price change.*  

```csharp  
var client = new OKXSocketClient();  
var result = await client.UnifiedApi.SubscribeToEstimatedPriceUpdatesAsync(/* parameters */);  
```  

```csharp  
Task<CallResult<UpdateSubscription>> SubscribeToEstimatedPriceUpdatesAsync(OKXInstrumentType instrumentType, string underlying, Action<OKXEstimatedPrice> onData, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|instrumentType|Instrument Type|
|underlying|Underlying|
|onData|On Data Handler|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## SubscribeToFundingRateUpdatesAsync  

[https://www.okx.com/docs-v5/en/#public-data-websocket-funding-rate-channel](https://www.okx.com/docs-v5/en/#public-data-websocket-funding-rate-channel)  
<p>

*Subscribe to funding rate updates. Data will be pushed every minute.*  

```csharp  
var client = new OKXSocketClient();  
var result = await client.UnifiedApi.SubscribeToFundingRateUpdatesAsync(/* parameters */);  
```  

```csharp  
Task<CallResult<UpdateSubscription>> SubscribeToFundingRateUpdatesAsync(string symbol, Action<OKXFundingRate> onData, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|symbol|Symbol|
|onData|On Data Handler|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## SubscribeToIndexKlineUpdatesAsync  

[https://www.okx.com/docs-v5/en/#public-data-websocket-index-candlesticks-channel](https://www.okx.com/docs-v5/en/#public-data-websocket-index-candlesticks-channel)  
<p>

*Subscribe to the candlesticks data of the index updates. Data will be pushed every 500 ms.*  

```csharp  
var client = new OKXSocketClient();  
var result = await client.UnifiedApi.SubscribeToIndexKlineUpdatesAsync(/* parameters */);  
```  

```csharp  
Task<CallResult<UpdateSubscription>> SubscribeToIndexKlineUpdatesAsync(string symbol, OKXPeriod period, Action<OKXCandlestick> onData, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|symbol|Symbol|
|period|Period|
|onData|On Data Handler|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## SubscribeToIndexTickerUpdatesAsync  

[https://www.okx.com/docs-v5/en/#public-data-websocket-index-tickers-channel](https://www.okx.com/docs-v5/en/#public-data-websocket-index-tickers-channel)  
<p>

*Subscribe to index tickers data updates*  

```csharp  
var client = new OKXSocketClient();  
var result = await client.UnifiedApi.SubscribeToIndexTickerUpdatesAsync(/* parameters */);  
```  

```csharp  
Task<CallResult<UpdateSubscription>> SubscribeToIndexTickerUpdatesAsync(string symbol, Action<OKXIndexTicker> onData, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|symbol|Symbol|
|onData|On Data Handler|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## SubscribeToKlineUpdatesAsync  

[https://www.okx.com/docs-v5/en/#order-book-trading-market-data-ws-candlesticks-channel](https://www.okx.com/docs-v5/en/#order-book-trading-market-data-ws-candlesticks-channel)  
<p>

*Subscribe to the candlesticks data updates of a symbol. Data will be pushed every 500 ms.*  

```csharp  
var client = new OKXSocketClient();  
var result = await client.UnifiedApi.SubscribeToKlineUpdatesAsync(/* parameters */);  
```  

```csharp  
Task<CallResult<UpdateSubscription>> SubscribeToKlineUpdatesAsync(string symbol, OKXPeriod period, Action<OKXCandlestick> onData, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|symbol|Symbol|
|period||
|onData|On Data Handler|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## SubscribeToMarkPriceKlineUpdatesAsync  

[https://www.okx.com/docs-v5/en/#public-data-websocket-mark-price-candlesticks-channel](https://www.okx.com/docs-v5/en/#public-data-websocket-mark-price-candlesticks-channel)  
<p>

*Subscribe to the candlesticks data updates of the mark price. Data will be pushed every 500 ms.*  

```csharp  
var client = new OKXSocketClient();  
var result = await client.UnifiedApi.SubscribeToMarkPriceKlineUpdatesAsync(/* parameters */);  
```  

```csharp  
Task<CallResult<UpdateSubscription>> SubscribeToMarkPriceKlineUpdatesAsync(string symbol, OKXPeriod period, Action<OKXCandlestick> onData, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|symbol|Symbol|
|period|Period|
|onData|On Data Handler|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## SubscribeToMarkPriceUpdatesAsync  

[https://www.okx.com/docs-v5/en/#public-data-websocket-mark-price-channel](https://www.okx.com/docs-v5/en/#public-data-websocket-mark-price-channel)  
<p>

*Subscribe to the mark price updates. Data will be pushed every 200 ms when the mark price changes, and will be pushed every 10 seconds when the mark price does not change.*  

```csharp  
var client = new OKXSocketClient();  
var result = await client.UnifiedApi.SubscribeToMarkPriceUpdatesAsync(/* parameters */);  
```  

```csharp  
Task<CallResult<UpdateSubscription>> SubscribeToMarkPriceUpdatesAsync(string symbol, Action<OKXMarkPrice> onData, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|symbol|Symbol|
|onData|On Data Handler|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## SubscribeToOpenInterestUpdatesAsync  

[https://www.okx.com/docs-v5/en/#public-data-websocket-open-interest-channel](https://www.okx.com/docs-v5/en/#public-data-websocket-open-interest-channel)  
<p>

*Subscribe to the open interest updates. Data will by pushed every 3 seconds.*  

```csharp  
var client = new OKXSocketClient();  
var result = await client.UnifiedApi.SubscribeToOpenInterestUpdatesAsync(/* parameters */);  
```  

```csharp  
Task<CallResult<UpdateSubscription>> SubscribeToOpenInterestUpdatesAsync(string symbol, Action<OKXOpenInterest> onData, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|symbol|Symbol|
|onData|On Data Handler|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## SubscribeToOptionSummaryUpdatesAsync  

[https://www.okx.com/docs-v5/en/#public-data-websocket-option-summary-channel](https://www.okx.com/docs-v5/en/#public-data-websocket-option-summary-channel)  
<p>

*Subscribe to detailed pricing information updates of all OPTION contracts. Data will be pushed at once.*  

```csharp  
var client = new OKXSocketClient();  
var result = await client.UnifiedApi.SubscribeToOptionSummaryUpdatesAsync(/* parameters */);  
```  

```csharp  
Task<CallResult<UpdateSubscription>> SubscribeToOptionSummaryUpdatesAsync(string underlying, Action<OKXOptionSummary> onData, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|underlying|Underlying|
|onData|On Data Handler|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## SubscribeToOrderBookUpdatesAsync  

[https://www.okx.com/docs-v5/en/#order-book-trading-market-data-ws-order-book-channel](https://www.okx.com/docs-v5/en/#order-book-trading-market-data-ws-order-book-channel)  
<p>

*Subscribe to order book data updates.*  
*Use books for 400 depth levels, book5 for 5 depth levels, books50-l2-tbt tick-by-tick 50 depth levels, and books-l2-tbt for tick-by-tick 400 depth levels.*  
*books: 400 depth levels will be pushed in the initial full snapshot. Incremental data will be pushed every 100 ms when there is change in order book.*  
*books5: 5 depth levels will be pushed every time.Data will be pushed every 200 ms when there is change in order book.*  
*books50-l2-tbt: 50 depth levels will be pushed in the initial full snapshot. Incremental data will be pushed tick by tick, i.e.whenever there is change in order book.*  
*books-l2-tbt: 400 depth levels will be pushed in the initial full snapshot. Incremental data will be pushed tick by tick, i.e.whenever there is change in order book.*  

```csharp  
var client = new OKXSocketClient();  
var result = await client.UnifiedApi.SubscribeToOrderBookUpdatesAsync(/* parameters */);  
```  

```csharp  
Task<CallResult<UpdateSubscription>> SubscribeToOrderBookUpdatesAsync(string symbol, OKXOrderBookType orderBookType, Action<DataEvent<OKXOrderBook>> onData, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|symbol|Symbol|
|orderBookType|Order Book Type|
|onData|On Data Handler|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## SubscribeToOrderUpdatesAsync  

[https://www.okx.com/docs-v5/en/#order-book-trading-trade-ws-order-channel](https://www.okx.com/docs-v5/en/#order-book-trading-trade-ws-order-channel)  
<p>

*Subscribe to order information updates. Data will not be pushed when first subscribed. Data will only be pushed when triggered by events such as placing/canceling order.*  

```csharp  
var client = new OKXSocketClient();  
var result = await client.UnifiedApi.SubscribeToOrderUpdatesAsync(/* parameters */);  
```  

```csharp  
Task<CallResult<UpdateSubscription>> SubscribeToOrderUpdatesAsync(OKXInstrumentType instrumentType, string? symbol, string? underlying, Action<OKXOrder> onData, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|instrumentType|Instrument Type|
|symbol|Symbol|
|underlying|Underlying|
|onData|On Data Handler|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## SubscribeToPositionUpdatesAsync  

[https://www.okx.com/docs-v5/en/#trading-account-websocket-positions-channel](https://www.okx.com/docs-v5/en/#trading-account-websocket-positions-channel)  
<p>

*Subscribe to position information updates. Initial snapshot will be pushed according to subscription granularity. Data will be pushed when triggered by events such as placing/canceling order, and will also be pushed in regular interval according to subscription granularity.*  

```csharp  
var client = new OKXSocketClient();  
var result = await client.UnifiedApi.SubscribeToPositionUpdatesAsync(/* parameters */);  
```  

```csharp  
Task<CallResult<UpdateSubscription>> SubscribeToPositionUpdatesAsync(OKXInstrumentType instrumentType, string symbol, string underlying, Action<OKXPosition> onData, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|instrumentType|Instrument Type|
|symbol|Instrument ID|
|underlying|Underlying|
|onData|On Data Handler|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## SubscribeToPriceLimitUpdatesAsync  

[https://www.okx.com/docs-v5/en/#public-data-websocket-price-limit-channel](https://www.okx.com/docs-v5/en/#public-data-websocket-price-limit-channel)  
<p>

*Subscribe to the maximum buy price and minimum sell price of the instrument updates. Data will be pushed every 5 seconds when there are changes in limits, and will not be pushed when there is no changes on limit.*  

```csharp  
var client = new OKXSocketClient();  
var result = await client.UnifiedApi.SubscribeToPriceLimitUpdatesAsync(/* parameters */);  
```  

```csharp  
Task<CallResult<UpdateSubscription>> SubscribeToPriceLimitUpdatesAsync(string symbol, Action<OKXLimitPrice> onData, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|symbol|Symbol|
|onData|On Data Handler|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## SubscribeToSymbolUpdatesAsync  

[https://www.okx.com/docs-v5/en/#public-data-websocket-instruments-channel](https://www.okx.com/docs-v5/en/#public-data-websocket-instruments-channel)  
<p>

*Subscribe to symbols updates. The instruments will be pushed if there's any change to the instrument’s state (such as delivery of FUTURES, exercise of OPTION, listing of new contracts / trading pairs, trading suspension, etc.).*  

```csharp  
var client = new OKXSocketClient();  
var result = await client.UnifiedApi.SubscribeToSymbolUpdatesAsync(/* parameters */);  
```  

```csharp  
Task<CallResult<UpdateSubscription>> SubscribeToSymbolUpdatesAsync(OKXInstrumentType instrumentType, Action<OKXInstrument> onData, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|instrumentType|Instrument Type|
|onData|On Data Handler|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## SubscribeToSystemStatusUpdatesAsync  

[https://www.okx.com/docs-v5/en/#status-ws-status-channel](https://www.okx.com/docs-v5/en/#status-ws-status-channel)  
<p>

*Subscribe to status updates of system maintenance and push when the system maintenance status changes. First subscription: "Push the latest change data"; every time there is a state change, push the changed content*  

```csharp  
var client = new OKXSocketClient();  
var result = await client.UnifiedApi.SubscribeToSystemStatusUpdatesAsync(/* parameters */);  
```  

```csharp  
Task<CallResult<UpdateSubscription>> SubscribeToSystemStatusUpdatesAsync(Action<OKXStatus> onData, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|onData|On Data Handler|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## SubscribeToTickerUpdatesAsync  

[https://www.okx.com/docs-v5/en/#order-book-trading-market-data-ws-tickers-channel](https://www.okx.com/docs-v5/en/#order-book-trading-market-data-ws-tickers-channel)  
<p>

*Subscribe to the last traded price updates, bid price, ask price and 24-hour trading volume of instruments. Data will be pushed every 100 ms.*  

```csharp  
var client = new OKXSocketClient();  
var result = await client.UnifiedApi.SubscribeToTickerUpdatesAsync(/* parameters */);  
```  

```csharp  
Task<CallResult<UpdateSubscription>> SubscribeToTickerUpdatesAsync(string symbol, Action<OKXTicker> onData, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|symbol|Symbol|
|onData|On Data Handler|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## SubscribeToTradeUpdatesAsync  

[https://www.okx.com/docs-v5/en/#order-book-trading-market-data-ws-trades-channel](https://www.okx.com/docs-v5/en/#order-book-trading-market-data-ws-trades-channel)  
<p>

*Subscribe to the recent trades data updates. Data will be pushed whenever there is a trade.*  

```csharp  
var client = new OKXSocketClient();  
var result = await client.UnifiedApi.SubscribeToTradeUpdatesAsync(/* parameters */);  
```  

```csharp  
Task<CallResult<UpdateSubscription>> SubscribeToTradeUpdatesAsync(string symbol, Action<OKXTrade> onData, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|symbol|Symbols|
|onData|On Data Handler|
|_[Optional]_ ct|Cancellation Token|

</p>
