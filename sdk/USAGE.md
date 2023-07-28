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