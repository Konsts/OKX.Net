---
title: IOKXRestClientUnifiedApiTrading
has_children: false
parent: IOKXRestClientUnifiedApi
grand_parent: Rest API documentation
---
*[generated documentation]*  
`OKXRestClient > UnifiedApi > Trading`  
*Unified API trading endpoints*
  

***

## AmendMultipleOrdersAsync  

[https://www.okx.com/docs-v5/en/#order-book-trading-trade-post-amend-multiple-orders](https://www.okx.com/docs-v5/en/#order-book-trading-trade-post-amend-multiple-orders)  
<p>

*Amend incomplete orders in batches. Maximum 20 orders can be amended at a time. Request parameters should be passed in the form of an array.*  

```csharp  
var client = new OKXRestClient();  
var result = await client.UnifiedApi.Trading.AmendMultipleOrdersAsync(/* parameters */);  
```  

```csharp  
Task<WebCallResult<IEnumerable<OKXOrderAmendResponse>>> AmendMultipleOrdersAsync(IEnumerable<OKXOrderAmendRequest> orders, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|orders|Orders|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## AmendOrderAsync  

[https://www.okx.com/docs-v5/en/#order-book-trading-trade-post-amend-order](https://www.okx.com/docs-v5/en/#order-book-trading-trade-post-amend-order)  
<p>

*Amend an incomplete order.*  

```csharp  
var client = new OKXRestClient();  
var result = await client.UnifiedApi.Trading.AmendOrderAsync(/* parameters */);  
```  

```csharp  
Task<WebCallResult<OKXOrderAmendResponse>> AmendOrderAsync(string symbol, long? orderId = default, string? clientOrderId = default, string? requestId = default, bool? cancelOnFail = default, decimal? newQuantity = default, decimal? newPrice = default, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|symbol|Instrument ID|
|_[Optional]_ orderId|Order ID|
|_[Optional]_ clientOrderId|Client Order ID|
|_[Optional]_ requestId|Request ID|
|_[Optional]_ cancelOnFail|Cancel On Fail|
|_[Optional]_ newQuantity|New Quantity|
|_[Optional]_ newPrice|New Price|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## CancelAdvanceAlgoOrderAsync  

[https://www.okx.com/docs-v5/en/#order-book-trading-algo-trading-post-cancel-algo-order](https://www.okx.com/docs-v5/en/#order-book-trading-algo-trading-post-cancel-algo-order)  
<p>

*Cancel unfilled algo orders(iceberg order and twap order). A maximum of 10 orders can be canceled at a time. Request parameters should be passed in the form of an array.*  

```csharp  
var client = new OKXRestClient();  
var result = await client.UnifiedApi.Trading.CancelAdvanceAlgoOrderAsync(/* parameters */);  
```  

```csharp  
Task<WebCallResult<OKXAlgoOrderResponse>> CancelAdvanceAlgoOrderAsync(IEnumerable<OKXAlgoOrderRequest> orders, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|orders|Orders|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## CancelAlgoOrderAsync  

[]()  
<p>

*Cancel unfilled algo orders(trigger order, oco order, conditional order). A maximum of 10 orders can be canceled at a time. Request parameters should be passed in the form of an array.*  

```csharp  
var client = new OKXRestClient();  
var result = await client.UnifiedApi.Trading.CancelAlgoOrderAsync(/* parameters */);  
```  

```csharp  
Task<WebCallResult<OKXAlgoOrderResponse>> CancelAlgoOrderAsync(IEnumerable<OKXAlgoOrderRequest> orders, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|orders|Orders|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## CancelMultipleOrdersAsync  

[https://www.okx.com/docs-v5/en/#order-book-trading-trade-post-cancel-multiple-orders](https://www.okx.com/docs-v5/en/#order-book-trading-trade-post-cancel-multiple-orders)  
<p>

*Cancel incomplete orders in batches. Maximum 20 orders can be canceled at a time. Request parameters should be passed in the form of an array.*  

```csharp  
var client = new OKXRestClient();  
var result = await client.UnifiedApi.Trading.CancelMultipleOrdersAsync(/* parameters */);  
```  

```csharp  
Task<WebCallResult<IEnumerable<OKXOrderCancelResponse>>> CancelMultipleOrdersAsync(IEnumerable<OKXOrderCancelRequest> orders, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|orders|Orders|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## CancelOrderAsync  

[https://www.okx.com/docs-v5/en/#order-book-trading-trade-post-cancel-order](https://www.okx.com/docs-v5/en/#order-book-trading-trade-post-cancel-order)  
<p>

*Cancel an incomplete order.*  

```csharp  
var client = new OKXRestClient();  
var result = await client.UnifiedApi.Trading.CancelOrderAsync(/* parameters */);  
```  

```csharp  
Task<WebCallResult<OKXOrderCancelResponse>> CancelOrderAsync(string symbol, long? orderId = default, string? clientOrderId = default, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|symbol|Symbol|
|_[Optional]_ orderId|Order ID|
|_[Optional]_ clientOrderId|Client Order ID|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## ClosePositionAsync  

[https://www.okx.com/docs-v5/en/#order-book-trading-trade-post-close-positions](https://www.okx.com/docs-v5/en/#order-book-trading-trade-post-close-positions)  
<p>

*Close all positions of an instrument via a market order.*  

```csharp  
var client = new OKXRestClient();  
var result = await client.UnifiedApi.Trading.ClosePositionAsync(/* parameters */);  
```  

```csharp  
Task<WebCallResult<OKXClosePositionResponse>> ClosePositionAsync(string symbol, OKXMarginMode marginMode, OKXPositionSide? positionSide = default, string? asset = default, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|symbol|Symbol|
|marginMode|Margin Mode|
|_[Optional]_ positionSide|Position Side|
|_[Optional]_ asset|Asset|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## GetAlgoOrderHistoryAsync  

[https://www.okx.com/docs-v5/en/#order-book-trading-algo-trading-get-algo-order-history](https://www.okx.com/docs-v5/en/#order-book-trading-algo-trading-get-algo-order-history)  
<p>

*Retrieve a list of untriggered Algo orders under the current account.*  

```csharp  
var client = new OKXRestClient();  
var result = await client.UnifiedApi.Trading.GetAlgoOrderHistoryAsync(/* parameters */);  
```  

```csharp  
Task<WebCallResult<IEnumerable<OKXAlgoOrder>>> GetAlgoOrderHistoryAsync(OKXAlgoOrderType algoOrderType, OKXAlgoOrderState? algoOrderState = default, long? algoId = default, OKXInstrumentType? instrumentType = default, string? symbol = default, DateTime? startTime = default, DateTime? endTime = default, int limit, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|algoOrderType|Algo Order Type|
|_[Optional]_ algoOrderState|Algo Order State|
|_[Optional]_ algoId|Algo ID|
|_[Optional]_ instrumentType|Instrument Type|
|_[Optional]_ symbol|Symbol|
|_[Optional]_ startTime|Pagination of data to return records earlier than the requested ts|
|_[Optional]_ endTime|Pagination of data to return records newer than the requested ts|
|limit|Number of results per request. The maximum is 100; the default is 100.|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## GetAlgoOrderListAsync  

[https://www.okx.com/docs-v5/en/#order-book-trading-algo-trading-get-algo-order-list](https://www.okx.com/docs-v5/en/#order-book-trading-algo-trading-get-algo-order-list)  
<p>

*Cancel unfilled algo orders(iceberg order and twap order). A maximum of 10 orders can be canceled at a time. Request parameters should be passed in the form of an array.*  

```csharp  
var client = new OKXRestClient();  
var result = await client.UnifiedApi.Trading.GetAlgoOrderListAsync(/* parameters */);  
```  

```csharp  
Task<WebCallResult<IEnumerable<OKXAlgoOrder>>> GetAlgoOrderListAsync(OKXAlgoOrderType algoOrderType, long? algoId = default, OKXInstrumentType? instrumentType = default, string? symbol = default, DateTime? startTime = default, DateTime? endTime = default, int limit, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|algoOrderType|Algo Order Type|
|_[Optional]_ algoId|Algo ID|
|_[Optional]_ instrumentType|Instrument Type|
|_[Optional]_ symbol|Symbol|
|_[Optional]_ startTime|Pagination of data to return records earlier than the requested ts|
|_[Optional]_ endTime|Pagination of data to return records newer than the requested ts|
|limit|Number of results per request. The maximum is 100; the default is 100.|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## GetOrderArchiveAsync  

[https://www.okx.com/docs-v5/en/#order-book-trading-trade-get-order-history-last-3-months](https://www.okx.com/docs-v5/en/#order-book-trading-trade-get-order-history-last-3-months)  
<p>

*Retrieve the completed order data of the last 3 months, and the incomplete orders that have been canceled are only reserved for 2 hours.*  

```csharp  
var client = new OKXRestClient();  
var result = await client.UnifiedApi.Trading.GetOrderArchiveAsync(/* parameters */);  
```  

```csharp  
Task<WebCallResult<IEnumerable<OKXOrder>>> GetOrderArchiveAsync(OKXInstrumentType instrumentType, string? symbol = default, string? underlying = default, OKXOrderType? orderType = default, OKXOrderState? state = default, OKXOrderCategory? category = default, DateTime? startTime = default, DateTime? endTime = default, int limit, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|instrumentType|Instrument Type|
|_[Optional]_ symbol|Symbol|
|_[Optional]_ underlying|Underlying|
|_[Optional]_ orderType|Order Type|
|_[Optional]_ state|State|
|_[Optional]_ category|Category|
|_[Optional]_ startTime|Pagination of data to return records earlier than the requested ts|
|_[Optional]_ endTime|Pagination of data to return records newer than the requested ts|
|limit|Number of results per request. The maximum is 100; the default is 100.|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## GetOrderDetailsAsync  

[https://www.okx.com/docs-v5/en/#order-book-trading-trade-get-order-details](https://www.okx.com/docs-v5/en/#order-book-trading-trade-get-order-details)  
<p>

*Retrieve order details.*  

```csharp  
var client = new OKXRestClient();  
var result = await client.UnifiedApi.Trading.GetOrderDetailsAsync(/* parameters */);  
```  

```csharp  
Task<WebCallResult<OKXOrder>> GetOrderDetailsAsync(string symbol, long? orderId = default, string? clientOrderId = default, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|symbol|Instrument ID|
|_[Optional]_ orderId|Order ID|
|_[Optional]_ clientOrderId|Client Order ID|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## GetOrderHistoryAsync  

[https://www.okx.com/docs-v5/en/#order-book-trading-trade-get-order-history-last-7-days](https://www.okx.com/docs-v5/en/#order-book-trading-trade-get-order-history-last-7-days)  
<p>

*Retrieve the completed order data for the last 7 days, and the incomplete orders that have been cancelled are only reserved for 2 hours.*  

```csharp  
var client = new OKXRestClient();  
var result = await client.UnifiedApi.Trading.GetOrderHistoryAsync(/* parameters */);  
```  

```csharp  
Task<WebCallResult<IEnumerable<OKXOrder>>> GetOrderHistoryAsync(OKXInstrumentType instrumentType, string? symbol = default, string? underlying = default, OKXOrderType? orderType = default, OKXOrderState? state = default, OKXOrderCategory? category = default, DateTime? startTime = default, DateTime? endTime = default, int limit, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|instrumentType|Instrument Type|
|_[Optional]_ symbol|Instrument ID|
|_[Optional]_ underlying|Underlying|
|_[Optional]_ orderType|Order Type|
|_[Optional]_ state|State|
|_[Optional]_ category|Category|
|_[Optional]_ startTime|Pagination of data to return records earlier than the requested ts|
|_[Optional]_ endTime|Pagination of data to return records newer than the requested ts|
|limit|Number of results per request. The maximum is 100; the default is 100.|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## GetOrdersAsync  

[https://www.okx.com/docs-v5/en/#order-book-trading-trade-get-order-list](https://www.okx.com/docs-v5/en/#order-book-trading-trade-get-order-list)  
<p>

*Retrieve all incomplete orders under the current account.*  

```csharp  
var client = new OKXRestClient();  
var result = await client.UnifiedApi.Trading.GetOrdersAsync(/* parameters */);  
```  

```csharp  
Task<WebCallResult<IEnumerable<OKXOrder>>> GetOrdersAsync(OKXInstrumentType? instrumentType = default, string? symbol = default, string? underlying = default, OKXOrderType? orderType = default, OKXOrderState? state = default, DateTime? startTime = default, DateTime? endTime = default, int limit, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|_[Optional]_ instrumentType|Instrument Type|
|_[Optional]_ symbol|Instrument ID|
|_[Optional]_ underlying|Underlying|
|_[Optional]_ orderType|Order Type|
|_[Optional]_ state|State|
|_[Optional]_ startTime|Pagination of data to return records earlier than the requested ts|
|_[Optional]_ endTime|Pagination of data to return records newer than the requested ts|
|limit|Number of results per request. The maximum is 100; the default is 100.|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## GetUserTradesArchiveAsync  

[https://www.okx.com/docs-v5/en/#order-book-trading-trade-get-transaction-details-last-3-months](https://www.okx.com/docs-v5/en/#order-book-trading-trade-get-transaction-details-last-3-months)  
<p>

*Retrieve recently-filled transaction details in the last 3 months.*  

```csharp  
var client = new OKXRestClient();  
var result = await client.UnifiedApi.Trading.GetUserTradesArchiveAsync(/* parameters */);  
```  

```csharp  
Task<WebCallResult<IEnumerable<OKXTransaction>>> GetUserTradesArchiveAsync(OKXInstrumentType instrumentType, string? symbol = default, string? underlying = default, long? orderId = default, DateTime? startTime = default, DateTime? endTime = default, int limit, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|instrumentType|Instrument Type|
|_[Optional]_ symbol|Symbol|
|_[Optional]_ underlying|Underlying|
|_[Optional]_ orderId|Order ID|
|_[Optional]_ startTime|Pagination of data to return records earlier than the requested ts|
|_[Optional]_ endTime|Pagination of data to return records newer than the requested ts|
|limit|Number of results per request. The maximum is 100; the default is 100.|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## GetUserTradesAsync  

[https://www.okx.com/docs-v5/en/#order-book-trading-trade-get-transaction-details-last-3-days](https://www.okx.com/docs-v5/en/#order-book-trading-trade-get-transaction-details-last-3-days)  
<p>

*Retrieve recently-filled transaction details in the last 3 day.*  

```csharp  
var client = new OKXRestClient();  
var result = await client.UnifiedApi.Trading.GetUserTradesAsync(/* parameters */);  
```  

```csharp  
Task<WebCallResult<IEnumerable<OKXTransaction>>> GetUserTradesAsync(OKXInstrumentType? instrumentType = default, string? symbol = default, string? underlying = default, long? orderId = default, DateTime? startTime = default, DateTime? endTime = default, int limit, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|_[Optional]_ instrumentType|Instrument Type|
|_[Optional]_ symbol|Symbol|
|_[Optional]_ underlying|Underlying|
|_[Optional]_ orderId|Order ID|
|_[Optional]_ startTime|Pagination of data to return records earlier than the requested ts|
|_[Optional]_ endTime|Pagination of data to return records newer than the requested ts|
|limit|Number of results per request. The maximum is 100; the default is 100.|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## PlaceAlgoOrderAsync  

[https://www.okx.com/docs-v5/en/#order-book-trading-algo-trading-post-place-algo-order](https://www.okx.com/docs-v5/en/#order-book-trading-algo-trading-post-place-algo-order)  
<p>

*The algo order includes trigger order, oco order, conditional order,iceberg order and twap order.*  

```csharp  
var client = new OKXRestClient();  
var result = await client.UnifiedApi.Trading.PlaceAlgoOrderAsync(/* parameters */);  
```  

```csharp  
Task<WebCallResult<OKXAlgoOrderResponse>> PlaceAlgoOrderAsync(string symbol, OKXTradeMode tradeMode, OKXOrderSide orderSide, OKXAlgoOrderType algoOrderType, decimal quantity, string? asset = default, bool? reduceOnly = default, OKXPositionSide? positionSide = default, OKXQuantityType? quantityType = default, OKXAlgoPriceType? tpTriggerPxType = default, decimal? tpTriggerPrice = default, decimal? tpOrderPrice = default, OKXAlgoPriceType? slTriggerPxType = default, decimal? slTriggerPrice = default, decimal? slOrderPrice = default, decimal? triggerPrice = default, decimal? orderPrice = default, OKXPriceVariance? pxVar = default, decimal? priceRatio = default, decimal? sizeLimit = default, decimal? priceLimit = default, long? timeInterval = default, decimal? callbackRatio = default, decimal? activePx = default, decimal? callbackSpread = default, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|symbol|Symbol|
|tradeMode|Trade Mode|
|orderSide|Order Side|
|algoOrderType|Algo Order Type|
|quantity|Quantity|
|_[Optional]_ asset|Asset|
|_[Optional]_ reduceOnly|Reduce Only|
|_[Optional]_ positionSide|Position Side|
|_[Optional]_ quantityType|Quantity Type|
|_[Optional]_ tpTriggerPxType|Take-profit trigger price type|
|_[Optional]_ tpTriggerPrice|Take Profit Trigger Price|
|_[Optional]_ tpOrderPrice|Take Profit Order Price|
|_[Optional]_ slTriggerPxType|Stop-loss trigger price. If you fill in this parameter, you should fill in the stop-loss order price.|
|_[Optional]_ slTriggerPrice|Stop Loss Trigger Price|
|_[Optional]_ slOrderPrice|Stop Loss Order Price|
|_[Optional]_ triggerPrice|Trigger Price|
|_[Optional]_ orderPrice|Order Price|
|_[Optional]_ pxVar|Price Variance|
|_[Optional]_ priceRatio|Price Ratio|
|_[Optional]_ sizeLimit|Size Limit|
|_[Optional]_ priceLimit|Price Limit|
|_[Optional]_ timeInterval|Time Interval|
|_[Optional]_ callbackRatio|Callback ratio|
|_[Optional]_ activePx|Active price|
|_[Optional]_ callbackSpread|Callback spread|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## PlaceMultipleOrdersAsync  

[https://www.okx.com/docs-v5/en/#order-book-trading-trade-post-place-multiple-orders](https://www.okx.com/docs-v5/en/#order-book-trading-trade-post-place-multiple-orders)  
<p>

*Place orders in batches. Maximum 20 orders can be placed at a time. Request parameters should be passed in the form of an array.*  

```csharp  
var client = new OKXRestClient();  
var result = await client.UnifiedApi.Trading.PlaceMultipleOrdersAsync(/* parameters */);  
```  

```csharp  
Task<WebCallResult<IEnumerable<OKXOrderPlaceResponse>>> PlaceMultipleOrdersAsync(IEnumerable<OKXOrderPlaceRequest> orders, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|orders|Orders|
|_[Optional]_ ct|Cancellation Token|

</p>

***

## PlaceOrderAsync  

[https://www.okx.com/docs-v5/en/#order-book-trading-trade-post-place-order](https://www.okx.com/docs-v5/en/#order-book-trading-trade-post-place-order)  
<p>

*You can place an order only if you have sufficient funds.*  

```csharp  
var client = new OKXRestClient();  
var result = await client.UnifiedApi.Trading.PlaceOrderAsync(/* parameters */);  
```  

```csharp  
Task<WebCallResult<OKXOrderPlaceResponse>> PlaceOrderAsync(string symbol, OKXOrderSide side, OKXOrderType type, decimal quantity, decimal? price = default, OKXPositionSide? positionSide = default, OKXTradeMode? tradeMode = default, decimal? takeProfitTriggerPrice = default, decimal? stopLossTriggerPrice = default, decimal? takeProfitOrderPrice = default, decimal? stopLossOrderPrice = default, OXKTriggerPriceType? takeProfitTriggerPriceType = default, OXKTriggerPriceType? stopLossTriggerPriceType = default, OKXQuickMarginType? quickMarginType = default, int? selfTradePreventionId = default, SelfTradePreventionMode? selfTradePreventionMode = default, string? asset = default, OKXQuantityAsset? quantityAsset = default, string? clientOrderId = default, bool? reduceOnly = default, OKXQuantityType? quantityType = default, CancellationToken ct = default);  
```  

|Parameter|Description|
|---|---|
|symbol|Symbol|
|side|Order Side|
|type|Order Type|
|quantity|Quantity|
|_[Optional]_ price|Price|
|_[Optional]_ positionSide|Position Side|
|_[Optional]_ tradeMode|Trade Mode|
|_[Optional]_ takeProfitTriggerPrice|Take profit trigger price|
|_[Optional]_ stopLossTriggerPrice|Stop loss trigger price|
|_[Optional]_ takeProfitOrderPrice|Take profit order price|
|_[Optional]_ stopLossOrderPrice|Stop loss order price|
|_[Optional]_ takeProfitTriggerPriceType|Take profit price type|
|_[Optional]_ stopLossTriggerPriceType|Stop loss price type|
|_[Optional]_ quickMarginType|Quick margin type|
|_[Optional]_ selfTradePreventionId|Self trade prevention id|
|_[Optional]_ selfTradePreventionMode|Self trade prevention mode|
|_[Optional]_ asset|Asset|
|_[Optional]_ quantityAsset|Asset of the quantity when placing market order|
|_[Optional]_ clientOrderId|Client Order ID|
|_[Optional]_ reduceOnly|Whether to reduce position only or not, true false, the default is false.|
|_[Optional]_ quantityType|Quantity Type|
|_[Optional]_ ct|Cancellation Token|

</p>
