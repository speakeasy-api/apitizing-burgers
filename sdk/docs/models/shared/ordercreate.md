# OrderCreate

Fields to create an order


## Fields

| Field                           | Type                            | Required                        | Description                     | Example                         |
| ------------------------------- | ------------------------------- | ------------------------------- | ------------------------------- | ------------------------------- |
| `burger_ids`                    | list[*int*]                     | :heavy_check_mark:              | List of burger ids in the order |                                 |
| `note`                          | *Optional[str]*                 | :heavy_minus_sign:              | Note for the order              | No onions                       |
| `table`                         | *int*                           | :heavy_check_mark:              | Table number for the order      | 1                               |