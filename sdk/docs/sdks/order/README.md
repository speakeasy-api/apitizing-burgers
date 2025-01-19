# Order
(*order*)

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
from openapi import SDK

with SDK(
    api_key="<YOUR_API_KEY_HERE>",
) as sdk:

    res = sdk.order.create_order(burger_ids=[
        1,
        3,
    ], table=2, note="No onions")

    # Handle response
    print(res)

```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         | Example                                                             |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `burger_ids`                                                        | List[*int*]                                                         | :heavy_check_mark:                                                  | List of burger ids in the order                                     | [<br/>1,<br/>2<br/>]                                                |
| `table`                                                             | *int*                                                               | :heavy_check_mark:                                                  | Table number for the order                                          | 1                                                                   |
| `note`                                                              | *Optional[str]*                                                     | :heavy_minus_sign:                                                  | Note for the order                                                  | No onions                                                           |
| `retries`                                                           | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)    | :heavy_minus_sign:                                                  | Configuration to override the default retry behavior of the client. |                                                                     |

### Response

**[models.OrderOutput](../../models/orderoutput.md)**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.HTTPValidationError | 422                        | application/json           |
| models.APIError            | 4XX, 5XX                   | \*/\*                      |

## list_orders

List all orders

### Example Usage

```python
from openapi import SDK

with SDK(
    api_key="<YOUR_API_KEY_HERE>",
) as sdk:

    res = sdk.order.list_orders()

    # Handle response
    print(res)

```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `retries`                                                           | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)    | :heavy_minus_sign:                                                  | Configuration to override the default retry behavior of the client. |

### Response

**[List[models.OrderOutput]](../../models/.md)**

### Errors

| Error Type      | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| models.APIError | 4XX, 5XX        | \*/\*           |

## read_order

Read an order

### Example Usage

```python
from openapi import SDK

with SDK(
    api_key="<YOUR_API_KEY_HERE>",
) as sdk:

    res = sdk.order.read_order(order_id=816257)

    # Handle response
    print(res)

```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `order_id`                                                          | *int*                                                               | :heavy_check_mark:                                                  | N/A                                                                 |
| `retries`                                                           | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)    | :heavy_minus_sign:                                                  | Configuration to override the default retry behavior of the client. |

### Response

**[models.OrderOutput](../../models/orderoutput.md)**

### Errors

| Error Type                  | Status Code                 | Content Type                |
| --------------------------- | --------------------------- | --------------------------- |
| models.ResponseMessageError | 404                         | application/json            |
| models.HTTPValidationError  | 422                         | application/json            |
| models.APIError             | 4XX, 5XX                    | \*/\*                       |

## update_order

Update an order

### Example Usage

```python
from openapi import SDK

with SDK(
    api_key="<YOUR_API_KEY_HERE>",
) as sdk:

    res = sdk.order.update_order(order_id=983384, burger_ids=[
        1,
        3,
    ], note="No onions", table=2)

    # Handle response
    print(res)

```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         | Example                                                             |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `order_id`                                                          | *int*                                                               | :heavy_check_mark:                                                  | N/A                                                                 |                                                                     |
| `burger_ids`                                                        | List[*int*]                                                         | :heavy_minus_sign:                                                  | List of burger ids in the order                                     | [<br/>1,<br/>2<br/>]                                                |
| `note`                                                              | *Optional[str]*                                                     | :heavy_minus_sign:                                                  | Note for the order                                                  | No onions                                                           |
| `status`                                                            | [Optional[models.OrderStatus]](../../models/orderstatus.md)         | :heavy_minus_sign:                                                  | Status of the order                                                 |                                                                     |
| `table`                                                             | *Optional[int]*                                                     | :heavy_minus_sign:                                                  | Table number for the order                                          | 1                                                                   |
| `retries`                                                           | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)    | :heavy_minus_sign:                                                  | Configuration to override the default retry behavior of the client. |                                                                     |

### Response

**[models.OrderOutput](../../models/orderoutput.md)**

### Errors

| Error Type                  | Status Code                 | Content Type                |
| --------------------------- | --------------------------- | --------------------------- |
| models.ResponseMessageError | 404                         | application/json            |
| models.HTTPValidationError  | 422                         | application/json            |
| models.APIError             | 4XX, 5XX                    | \*/\*                       |