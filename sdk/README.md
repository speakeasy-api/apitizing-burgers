# openapi

<!-- Start SDK Installation -->
## SDK Installation

```bash
pip install git+<UNSET>.git
```
<!-- End SDK Installation -->

## SDK Example Usage
<!-- Start SDK Example Usage -->


```python
import sdk
from sdk.models import shared

s = sdk.SDK()

req = shared.BurgerCreate(
    description='Veggie burger with avocado',
    name='Hamburger',
)

res = s.burger.create_burger(req)

if res.burger_output is not None:
    # handle response
```
<!-- End SDK Example Usage -->

<!-- Start SDK Available Operations -->
## Available Resources and Operations


### [burger](docs/sdks/burger/README.md)

* [create_burger](docs/sdks/burger/README.md#create_burger) - Create Burger
* [delete_burger](docs/sdks/burger/README.md#delete_burger) - Delete Burger
* [list_burgers](docs/sdks/burger/README.md#list_burgers) - List Burgers
* [read_burger](docs/sdks/burger/README.md#read_burger) - Read Burger
* [update_burger](docs/sdks/burger/README.md#update_burger) - Update Burger

### [order](docs/sdks/order/README.md)

* [create_order](docs/sdks/order/README.md#create_order) - Create Order
* [list_orders](docs/sdks/order/README.md#list_orders) - List Orders
* [read_order](docs/sdks/order/README.md#read_order) - Read Order
* [update_order](docs/sdks/order/README.md#update_order) - Update Order
<!-- End SDK Available Operations -->

### Maturity

This SDK is in beta, and there may be breaking changes between versions without a major version update. Therefore, we recommend pinning usage
to a specific package version. This way, you can install the same version each time without breaking changes unless you are intentionally
looking for the latest version.

### Contributions

While we value open-source contributions to this SDK, this library is generated programmatically.
Feel free to open a PR or a Github issue as a proof of concept and we'll do our best to include it in a future release!

### SDK Created by [Speakeasy](https://docs.speakeasyapi.dev/docs/using-speakeasy/client-sdks)
