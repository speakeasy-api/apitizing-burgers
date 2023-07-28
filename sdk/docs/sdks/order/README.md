# order

## Overview

Operations related to orders

### Available Operations

* [create_order](#create_order) - Create Order
* [list_orders](#list_orders) - List Orders
* [read_order](#read_order) - Read Order
* [update_order](#update_order) - Update Order

## create_order

Create an order

### Example Usage

```python
import sdk
from sdk.models import shared

s = sdk.SDK()

req = shared.OrderCreate(
    burger_ids=[
        645894,
        384382,
        437587,
    ],
    note='No onions',
    table=3,
)

res = s.order.create_order(req)

if res.order_output is not None:
    # handle response
```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `request`                                                           | [shared.OrderCreate](../../models/shared/ordercreate.md)            | :heavy_check_mark:                                                  | The request object to use for the request.                          |
| `retries`                                                           | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)    | :heavy_minus_sign:                                                  | Configuration to override the default retry behavior of the client. |


### Response

**[operations.CreateOrderResponse](../../models/operations/createorderresponse.md)**


## list_orders

List all orders

### Example Usage

```python
import sdk


s = sdk.SDK()


res = s.order.list_orders()

if res.order_outputs is not None:
    # handle response
```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `retries`                                                           | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)    | :heavy_minus_sign:                                                  | Configuration to override the default retry behavior of the client. |


### Response

**[operations.ListOrdersResponse](../../models/operations/listordersresponse.md)**


## read_order

Read an order

### Example Usage

```python
import sdk
from sdk.models import operations

s = sdk.SDK()

req = operations.ReadOrderRequest(
    order_id=56713,
)

res = s.order.read_order(req)

if res.order_output is not None:
    # handle response
```

### Parameters

| Parameter                                                                  | Type                                                                       | Required                                                                   | Description                                                                |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `request`                                                                  | [operations.ReadOrderRequest](../../models/operations/readorderrequest.md) | :heavy_check_mark:                                                         | The request object to use for the request.                                 |
| `retries`                                                                  | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)           | :heavy_minus_sign:                                                         | Configuration to override the default retry behavior of the client.        |


### Response

**[operations.ReadOrderResponse](../../models/operations/readorderresponse.md)**


## update_order

Update an order

### Example Usage

```python
import sdk
from sdk.models import operations, shared

s = sdk.SDK()

req = operations.UpdateOrderRequest(
    order_update=shared.OrderUpdate(
        burger_ids=[
            272656,
            383441,
            477665,
            791725,
        ],
        note='Extra ketchup',
        status=shared.OrderUpdateOrderStatus.READY,
        table=2,
    ),
    order_id=568045,
)

res = s.order.update_order(req)

if res.order_output is not None:
    # handle response
```

### Parameters

| Parameter                                                                      | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `request`                                                                      | [operations.UpdateOrderRequest](../../models/operations/updateorderrequest.md) | :heavy_check_mark:                                                             | The request object to use for the request.                                     |
| `retries`                                                                      | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)               | :heavy_minus_sign:                                                             | Configuration to override the default retry behavior of the client.            |


### Response

**[operations.UpdateOrderResponse](../../models/operations/updateorderresponse.md)**

