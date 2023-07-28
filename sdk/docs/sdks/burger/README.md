# burger

## Overview

Operations related to burgers

Burger external docs
<https://en.wikipedia.org/wiki/Hamburger>
### Available Operations

* [create_burger](#create_burger) - Create Burger
* [delete_burger](#delete_burger) - Delete Burger
* [list_burgers](#list_burgers) - List Burgers
* [read_burger](#read_burger) - Read Burger
* [update_burger](#update_burger) - Update Burger

## create_burger

Create a burger

### Example Usage

```python
import sdk
from sdk.models import shared

s = sdk.SDK()

req = shared.BurgerCreate(
    description='Veggie burger with avocado',
    name='Veggie Burger',
)

res = s.burger.create_burger(req)

if res.burger_output is not None:
    # handle response
```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `request`                                                           | [shared.BurgerCreate](../../models/shared/burgercreate.md)          | :heavy_check_mark:                                                  | The request object to use for the request.                          |
| `retries`                                                           | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)    | :heavy_minus_sign:                                                  | Configuration to override the default retry behavior of the client. |


### Response

**[operations.CreateBurgerResponse](../../models/operations/createburgerresponse.md)**


## delete_burger

Delete a burger

### Example Usage

```python
import sdk
from sdk.models import operations

s = sdk.SDK()

req = operations.DeleteBurgerRequest(
    burger_id=602763,
)

res = s.burger.delete_burger(req)

if res.response_message is not None:
    # handle response
```

### Parameters

| Parameter                                                                        | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `request`                                                                        | [operations.DeleteBurgerRequest](../../models/operations/deleteburgerrequest.md) | :heavy_check_mark:                                                               | The request object to use for the request.                                       |
| `retries`                                                                        | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)                 | :heavy_minus_sign:                                                               | Configuration to override the default retry behavior of the client.              |


### Response

**[operations.DeleteBurgerResponse](../../models/operations/deleteburgerresponse.md)**


## list_burgers

List all burgers

### Example Usage

```python
import sdk


s = sdk.SDK()


res = s.burger.list_burgers()

if res.burger_outputs is not None:
    # handle response
```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `retries`                                                           | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)    | :heavy_minus_sign:                                                  | Configuration to override the default retry behavior of the client. |


### Response

**[operations.ListBurgersResponse](../../models/operations/listburgersresponse.md)**


## read_burger

Read a burger

### Example Usage

```python
import sdk
from sdk.models import operations

s = sdk.SDK()

req = operations.ReadBurgerRequest(
    burger_id=857946,
)

res = s.burger.read_burger(req)

if res.burger_output is not None:
    # handle response
```

### Parameters

| Parameter                                                                    | Type                                                                         | Required                                                                     | Description                                                                  |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `request`                                                                    | [operations.ReadBurgerRequest](../../models/operations/readburgerrequest.md) | :heavy_check_mark:                                                           | The request object to use for the request.                                   |
| `retries`                                                                    | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)             | :heavy_minus_sign:                                                           | Configuration to override the default retry behavior of the client.          |


### Response

**[operations.ReadBurgerResponse](../../models/operations/readburgerresponse.md)**


## update_burger

Update a burger

### Example Usage

```python
import sdk
from sdk.models import operations, shared

s = sdk.SDK()

req = operations.UpdateBurgerRequest(
    burger_update=shared.BurgerUpdate(
        description='Veggie burger with avocado',
        name='null',
    ),
    burger_id=423655,
)

res = s.burger.update_burger(req)

if res.burger_output is not None:
    # handle response
```

### Parameters

| Parameter                                                                        | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `request`                                                                        | [operations.UpdateBurgerRequest](../../models/operations/updateburgerrequest.md) | :heavy_check_mark:                                                               | The request object to use for the request.                                       |
| `retries`                                                                        | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)                 | :heavy_minus_sign:                                                               | Configuration to override the default retry behavior of the client.              |


### Response

**[operations.UpdateBurgerResponse](../../models/operations/updateburgerresponse.md)**

